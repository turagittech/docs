
---
title: "getClientServiceAccountUser"
title_tag: "keycloak.openid.getClientServiceAccountUser"
meta_desc: "Documentation for the keycloak.openid.getClientServiceAccountUser function with examples, input properties, output properties, and supporting types."
layout: api
no_edit_this_page: true
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

This data source can be used to fetch information about the service account user that is associated with an OpenID client
that has service accounts enabled.


{{% examples %}}

## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}





{{< example csharp >}}

```csharp
using Pulumi;
using Keycloak = Pulumi.Keycloak;

class MyStack : Stack
{
    public MyStack()
    {
        var realm = new Keycloak.Realm("realm", new Keycloak.RealmArgs
        {
            Realm = "my-realm",
            Enabled = true,
        });
        var client = new Keycloak.OpenId.Client("client", new Keycloak.OpenId.ClientArgs
        {
            RealmId = realm.Id,
            ClientId = "client",
            AccessType = "CONFIDENTIAL",
            ServiceAccountsEnabled = true,
        });
        var serviceAccountUser = Output.Tuple(realm.Id, client.Id).Apply(values =>
        {
            var realmId = values.Item1;
            var clientId = values.Item2;
            return Keycloak.OpenId.GetClientServiceAccountUser.InvokeAsync(new Keycloak.OpenId.GetClientServiceAccountUserArgs
            {
                RealmId = realmId,
                ClientId = clientId,
            });
        });
        var offlineAccess = realm.Id.Apply(id => Keycloak.GetRole.InvokeAsync(new Keycloak.GetRoleArgs
        {
            RealmId = id,
            Name = "offline_access",
        }));
        var serviceAccountUserRoles = new Keycloak.UserRoles("serviceAccountUserRoles", new Keycloak.UserRolesArgs
        {
            RealmId = realm.Id,
            UserId = serviceAccountUser.Apply(serviceAccountUser => serviceAccountUser.Id),
            RoleIds = 
            {
                offlineAccess.Apply(offlineAccess => offlineAccess.Id),
            },
        });
    }

}
```


{{< /example >}}


{{< example go >}}

```go
package main

import (
	"github.com/pulumi/pulumi-keycloak/sdk/v4/go/keycloak"
	"github.com/pulumi/pulumi-keycloak/sdk/v4/go/keycloak/openid"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		realm, err := keycloak.NewRealm(ctx, "realm", &keycloak.RealmArgs{
			Realm:   pulumi.String("my-realm"),
			Enabled: pulumi.Bool(true),
		})
		if err != nil {
			return err
		}
		client, err := openid.NewClient(ctx, "client", &openid.ClientArgs{
			RealmId:                realm.ID(),
			ClientId:               pulumi.String("client"),
			AccessType:             pulumi.String("CONFIDENTIAL"),
			ServiceAccountsEnabled: pulumi.Bool(true),
		})
		if err != nil {
			return err
		}
		_, err = keycloak.NewUserRoles(ctx, "serviceAccountUserRoles", &keycloak.UserRolesArgs{
			RealmId: realm.ID(),
			UserId: serviceAccountUser.ApplyT(func(serviceAccountUser openid.GetClientServiceAccountUserResult) (string, error) {
				return serviceAccountUser.Id, nil
			}).(pulumi.StringOutput),
			RoleIds: pulumi.StringArray{
				offlineAccess.ApplyT(func(offlineAccess keycloak.LookupRoleResult) (string, error) {
					return offlineAccess.Id, nil
				}).(pulumi.StringOutput),
			},
		})
		if err != nil {
			return err
		}
		return nil
	})
}
```


{{< /example >}}


{{< example python >}}

```python
import pulumi
import pulumi_keycloak as keycloak

realm = keycloak.Realm("realm",
    realm="my-realm",
    enabled=True)
client = keycloak.openid.Client("client",
    realm_id=realm.id,
    client_id="client",
    access_type="CONFIDENTIAL",
    service_accounts_enabled=True)
service_account_user = pulumi.Output.all(realm.id, client.id).apply(lambda realmId, clientId: keycloak.openid.get_client_service_account_user(realm_id=realm_id,
    client_id=client_id))
offline_access = realm.id.apply(lambda id: keycloak.get_role(realm_id=id,
    name="offline_access"))
service_account_user_roles = keycloak.UserRoles("serviceAccountUserRoles",
    realm_id=realm.id,
    user_id=service_account_user.id,
    role_ids=[offline_access.id])
```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as keycloak from "@pulumi/keycloak";

const realm = new keycloak.Realm("realm", {
    realm: "my-realm",
    enabled: true,
});
const client = new keycloak.openid.Client("client", {
    realmId: realm.id,
    clientId: "client",
    accessType: "CONFIDENTIAL",
    serviceAccountsEnabled: true,
});
const serviceAccountUser = pulumi.all([realm.id, client.id]).apply(([realmId, clientId]) => keycloak.openid.getClientServiceAccountUser({
    realmId: realmId,
    clientId: clientId,
}));
const offlineAccess = realm.id.apply(id => keycloak.getRole({
    realmId: id,
    name: "offline_access",
}));
const serviceAccountUserRoles = new keycloak.UserRoles("serviceAccountUserRoles", {
    realmId: realm.id,
    userId: serviceAccountUser.id,
    roleIds: [offlineAccess.id],
});
```


{{< /example >}}





{{% /examples %}}




## Using getClientServiceAccountUser {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getClientServiceAccountUser<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetClientServiceAccountUserArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetClientServiceAccountUserResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>get_client_service_account_user(</span><span class="nx">client_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                                    <span class="nx">realm_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                                    <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> GetClientServiceAccountUserResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetClientServiceAccountUser<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">args</span><span class="p"> *</span><span class="nx">GetClientServiceAccountUserArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">GetClientServiceAccountUserResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `GetClientServiceAccountUser` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetClientServiceAccountUser </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetClientServiceAccountUserResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">GetClientServiceAccountUserArgs</span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="clientid_csharp">
<a href="#clientid_csharp" style="color: inherit; text-decoration: inherit;">Client<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the OpenID client with service accounts enabled.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="realmid_csharp">
<a href="#realmid_csharp" style="color: inherit; text-decoration: inherit;">Realm<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The realm that the OpenID client exists within.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="clientid_go">
<a href="#clientid_go" style="color: inherit; text-decoration: inherit;">Client<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the OpenID client with service accounts enabled.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="realmid_go">
<a href="#realmid_go" style="color: inherit; text-decoration: inherit;">Realm<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The realm that the OpenID client exists within.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="clientid_nodejs">
<a href="#clientid_nodejs" style="color: inherit; text-decoration: inherit;">client<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the OpenID client with service accounts enabled.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="realmid_nodejs">
<a href="#realmid_nodejs" style="color: inherit; text-decoration: inherit;">realm<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The realm that the OpenID client exists within.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="client_id_python">
<a href="#client_id_python" style="color: inherit; text-decoration: inherit;">client_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the OpenID client with service accounts enabled.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="realm_id_python">
<a href="#realm_id_python" style="color: inherit; text-decoration: inherit;">realm_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The realm that the OpenID client exists within.
{{% /md %}}</dd></dl>
{{% /choosable %}}




## getClientServiceAccountUser Result {#result}

The following output properties are available:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="attributes_csharp">
<a href="#attributes_csharp" style="color: inherit; text-decoration: inherit;">Attributes</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary&lt;string, object&gt;</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="clientid_csharp">
<a href="#clientid_csharp" style="color: inherit; text-decoration: inherit;">Client<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="email_csharp">
<a href="#email_csharp" style="color: inherit; text-decoration: inherit;">Email</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="emailverified_csharp">
<a href="#emailverified_csharp" style="color: inherit; text-decoration: inherit;">Email<wbr>Verified</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="enabled_csharp">
<a href="#enabled_csharp" style="color: inherit; text-decoration: inherit;">Enabled</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="federatedidentities_csharp">
<a href="#federatedidentities_csharp" style="color: inherit; text-decoration: inherit;">Federated<wbr>Identities</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getclientserviceaccountuserfederatedidentity">List&lt;Get<wbr>Client<wbr>Service<wbr>Account<wbr>User<wbr>Federated<wbr>Identity&gt;</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="firstname_csharp">
<a href="#firstname_csharp" style="color: inherit; text-decoration: inherit;">First<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_csharp">
<a href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="lastname_csharp">
<a href="#lastname_csharp" style="color: inherit; text-decoration: inherit;">Last<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="realmid_csharp">
<a href="#realmid_csharp" style="color: inherit; text-decoration: inherit;">Realm<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="username_csharp">
<a href="#username_csharp" style="color: inherit; text-decoration: inherit;">Username</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="attributes_go">
<a href="#attributes_go" style="color: inherit; text-decoration: inherit;">Attributes</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="clientid_go">
<a href="#clientid_go" style="color: inherit; text-decoration: inherit;">Client<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="email_go">
<a href="#email_go" style="color: inherit; text-decoration: inherit;">Email</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="emailverified_go">
<a href="#emailverified_go" style="color: inherit; text-decoration: inherit;">Email<wbr>Verified</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="enabled_go">
<a href="#enabled_go" style="color: inherit; text-decoration: inherit;">Enabled</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="federatedidentities_go">
<a href="#federatedidentities_go" style="color: inherit; text-decoration: inherit;">Federated<wbr>Identities</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getclientserviceaccountuserfederatedidentity">[]Get<wbr>Client<wbr>Service<wbr>Account<wbr>User<wbr>Federated<wbr>Identity</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="firstname_go">
<a href="#firstname_go" style="color: inherit; text-decoration: inherit;">First<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_go">
<a href="#id_go" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="lastname_go">
<a href="#lastname_go" style="color: inherit; text-decoration: inherit;">Last<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="realmid_go">
<a href="#realmid_go" style="color: inherit; text-decoration: inherit;">Realm<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="username_go">
<a href="#username_go" style="color: inherit; text-decoration: inherit;">Username</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="attributes_nodejs">
<a href="#attributes_nodejs" style="color: inherit; text-decoration: inherit;">attributes</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="clientid_nodejs">
<a href="#clientid_nodejs" style="color: inherit; text-decoration: inherit;">client<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="email_nodejs">
<a href="#email_nodejs" style="color: inherit; text-decoration: inherit;">email</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="emailverified_nodejs">
<a href="#emailverified_nodejs" style="color: inherit; text-decoration: inherit;">email<wbr>Verified</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="enabled_nodejs">
<a href="#enabled_nodejs" style="color: inherit; text-decoration: inherit;">enabled</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="federatedidentities_nodejs">
<a href="#federatedidentities_nodejs" style="color: inherit; text-decoration: inherit;">federated<wbr>Identities</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getclientserviceaccountuserfederatedidentity">Get<wbr>Client<wbr>Service<wbr>Account<wbr>User<wbr>Federated<wbr>Identity[]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="firstname_nodejs">
<a href="#firstname_nodejs" style="color: inherit; text-decoration: inherit;">first<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_nodejs">
<a href="#id_nodejs" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="lastname_nodejs">
<a href="#lastname_nodejs" style="color: inherit; text-decoration: inherit;">last<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="realmid_nodejs">
<a href="#realmid_nodejs" style="color: inherit; text-decoration: inherit;">realm<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="username_nodejs">
<a href="#username_nodejs" style="color: inherit; text-decoration: inherit;">username</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="attributes_python">
<a href="#attributes_python" style="color: inherit; text-decoration: inherit;">attributes</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Mapping[str, Any]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="client_id_python">
<a href="#client_id_python" style="color: inherit; text-decoration: inherit;">client_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="email_python">
<a href="#email_python" style="color: inherit; text-decoration: inherit;">email</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="email_verified_python">
<a href="#email_verified_python" style="color: inherit; text-decoration: inherit;">email_<wbr>verified</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="enabled_python">
<a href="#enabled_python" style="color: inherit; text-decoration: inherit;">enabled</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="federated_identities_python">
<a href="#federated_identities_python" style="color: inherit; text-decoration: inherit;">federated_<wbr>identities</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getclientserviceaccountuserfederatedidentity">Sequence[Get<wbr>Client<wbr>Service<wbr>Account<wbr>User<wbr>Federated<wbr>Identity]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="first_name_python">
<a href="#first_name_python" style="color: inherit; text-decoration: inherit;">first_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_python">
<a href="#id_python" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="last_name_python">
<a href="#last_name_python" style="color: inherit; text-decoration: inherit;">last_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="realm_id_python">
<a href="#realm_id_python" style="color: inherit; text-decoration: inherit;">realm_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="username_python">
<a href="#username_python" style="color: inherit; text-decoration: inherit;">username</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}




## Supporting Types


<h4 id="getclientserviceaccountuserfederatedidentity">Get<wbr>Client<wbr>Service<wbr>Account<wbr>User<wbr>Federated<wbr>Identity</h4>



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="identityprovider_csharp">
<a href="#identityprovider_csharp" style="color: inherit; text-decoration: inherit;">Identity<wbr>Provider</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="userid_csharp">
<a href="#userid_csharp" style="color: inherit; text-decoration: inherit;">User<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="username_csharp">
<a href="#username_csharp" style="color: inherit; text-decoration: inherit;">User<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="identityprovider_go">
<a href="#identityprovider_go" style="color: inherit; text-decoration: inherit;">Identity<wbr>Provider</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="userid_go">
<a href="#userid_go" style="color: inherit; text-decoration: inherit;">User<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="username_go">
<a href="#username_go" style="color: inherit; text-decoration: inherit;">User<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="identityprovider_nodejs">
<a href="#identityprovider_nodejs" style="color: inherit; text-decoration: inherit;">identity<wbr>Provider</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="userid_nodejs">
<a href="#userid_nodejs" style="color: inherit; text-decoration: inherit;">user<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="username_nodejs">
<a href="#username_nodejs" style="color: inherit; text-decoration: inherit;">user<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="identity_provider_python">
<a href="#identity_provider_python" style="color: inherit; text-decoration: inherit;">identity_<wbr>provider</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="user_id_python">
<a href="#user_id_python" style="color: inherit; text-decoration: inherit;">user_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="user_name_python">
<a href="#user_name_python" style="color: inherit; text-decoration: inherit;">user_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}





<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-keycloak">https://github.com/pulumi/pulumi-keycloak</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
	<dt>Notes</dt>
	<dd>{{% md %}}This Pulumi package is based on the [`keycloak` Terraform Provider](https://github.com/mrparkers/terraform-provider-keycloak).{{% /md %}}</dd>
</dl>
