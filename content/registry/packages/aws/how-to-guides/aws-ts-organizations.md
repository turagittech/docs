---
title: "AWS Organizations | TypeScript"
h1: "AWS Organizations"
linktitle: "AWS Organizations"
meta_desc: "AWS Organizations How-to Guide using TypeScript"
no_edit_this_page: true
cloud: aws
language: ts
layout: how-to-guide
---

<!-- WARNING: this page was generated by a tool. Do not edit it by hand. -->
<!-- To change it, please see https://github.com/pulumi/docs/tree/master/tools/mktutorial. -->

<p class="mb-4 flex">
    <a class="flex flex-wrap items-center rounded-md font-display text-lg text-white bg-blue-600 border-2 border-blue-600 px-2 mr-2 whitespace-no-wrap hover:text-white" style="height: 45px;" href="https://github.com/pulumi/examples/tree/master/aws-ts-organizations" target="_blank">
        <span><i class="fab fa-github pr-2"></i> View Code</span>
    </a>
</p>


[![Deploy](https://get.pulumi.com/new/button.svg)](https://app.pulumi.com/new?template=https://github.com/pulumi/examples/blob/master/aws-ts-organizations/README.md)

This example shows you how you can automate the creation of member accounts in AWS Organizations with Pulumi. This example is written in TypeScript, however, the concepts used within can be used with any of the supported SDKs in Pulumi. Read the associated [blog post](https://www.pulumi.com/blog/organizing-aws-accounts-with-pulumi) to learn more.

## Prerequisites

1. [Install Pulumi](https://www.pulumi.com/docs/get-started/install/)
1. [Configure Pulumi for AWS](https://www.pulumi.com/docs/intro/cloud-providers/aws/setup/)

### Enable policy types

This example also creates sample backup policy and tag policy at the organization unit-level.
You should first enable those policy types for your management account by navigating to the
AWS Organizations service > Policies, then click **Backup policies** as well as **Tag policies**
and enable them.

**Note**: This app requires credentials that have permissions to
AWS Organizations service. The IAM user running this app should
also be granted permissions to assume the role identified by `OrganizationalAccountAccessRole` in any account.

## Deploying and running the program

Note that unlike other resources that can be created/destroyed easily,
this app creates an AWS account and closed accounts are in a suspended state
for 90 days. That means, you won't be able to delete the organizational until until
the 90 days has elapsed.

1. Create a new stack:

    ```bash
    $ pulumi stack init accounts
    ```

1. Set the AWS region and the email contact to use for the dev AWS account that this app creates:

> The email contact for each member account needs to be unique. You can take advantage of email aliases
> that some email services provide by using the `+` character. Check with your email provider to see
> how if you can use email aliases.

    ```bash
    $ pulumi config set aws:region us-west-2
    $ pulumi config set devAccountEmailContact <email> --secret
    ```

1. Restore NPM modules via `npm install` or `yarn install`.

1. Run `pulumi up -y` to deploy changes.

Note that the flag to automatically close an account when the
associated resource is destroyed in Pulumi is set to `false`,
so the account won't be closed automatically. You can, of course,
change that flag in the code to `true` but that decision left
to you.

## Destroying the stack

Before you can destroy all the resoruces deployed by this stack with
a `pulumi destroy`, there are a couple of things to note.

1. The single AWS account that this example creates is protected from deletion
   by using Pulumi's `protect` resource option. That means, you should first tell
   Pulumi to release the protection. See the [docs](https://www.pulumi.com/docs/intro/concepts/resources/options/protect/)
   to learn how you can do that quickly.
1. As mentioned before, closed accounts will enter into in a suspended state for 90 days.
   That means you will encounter an error about not being able to delete the organizational
   unit (OU) despite having closed the AWS account that was under it. You will need to wait for 90 days
   before you can delete the OU.
