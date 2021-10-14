
---
title: "getTeam"
title_tag: "github.getTeam"
meta_desc: "Documentation for the github.getTeam function with examples, input properties, output properties, and supporting types."
layout: api
no_edit_this_page: true
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Use this data source to retrieve information about a GitHub team.


{{% examples %}}

## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}





{{< example csharp >}}

```csharp
using Pulumi;
using Github = Pulumi.Github;

class MyStack : Stack
{
    public MyStack()
    {
        var example = Output.Create(Github.GetTeam.InvokeAsync(new Github.GetTeamArgs
        {
            Slug = "example",
        }));
    }

}
```


{{< /example >}}


{{< example go >}}

```go
package main

import (
	"github.com/pulumi/pulumi-github/sdk/v4/go/github"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		_, err := github.LookupTeam(ctx, &github.LookupTeamArgs{
			Slug: "example",
		}, nil)
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
import pulumi_github as github

example = github.get_team(slug="example")
```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as github from "@pulumi/github";

const example = pulumi.output(github.getTeam({
    slug: "example",
}));
```


{{< /example >}}





{{% /examples %}}




## Using getTeam {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getTeam<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetTeamArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetTeamResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>get_team(</span><span class="nx">slug</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
             <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> GetTeamResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>LookupTeam<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">args</span><span class="p"> *</span><span class="nx">LookupTeamArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">LookupTeamResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `LookupTeam` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetTeam </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetTeamResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">GetTeamArgs</span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="slug_csharp">
<a href="#slug_csharp" style="color: inherit; text-decoration: inherit;">Slug</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The team slug.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="slug_go">
<a href="#slug_go" style="color: inherit; text-decoration: inherit;">Slug</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The team slug.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="slug_nodejs">
<a href="#slug_nodejs" style="color: inherit; text-decoration: inherit;">slug</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The team slug.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="slug_python">
<a href="#slug_python" style="color: inherit; text-decoration: inherit;">slug</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The team slug.
{{% /md %}}</dd></dl>
{{% /choosable %}}




## getTeam Result {#result}

The following output properties are available:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="description_csharp">
<a href="#description_csharp" style="color: inherit; text-decoration: inherit;">Description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}the team's description.
{{% /md %}}</dd><dt class="property-"
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
        <span id="members_csharp">
<a href="#members_csharp" style="color: inherit; text-decoration: inherit;">Members</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}List of team members
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}the team's full name.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="nodeid_csharp">
<a href="#nodeid_csharp" style="color: inherit; text-decoration: inherit;">Node<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}the Node ID of the team.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="permission_csharp">
<a href="#permission_csharp" style="color: inherit; text-decoration: inherit;">Permission</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}the team's permission level.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="privacy_csharp">
<a href="#privacy_csharp" style="color: inherit; text-decoration: inherit;">Privacy</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}the team's privacy type.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="repositories_csharp">
<a href="#repositories_csharp" style="color: inherit; text-decoration: inherit;">Repositories</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}List of team repositories
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="slug_csharp">
<a href="#slug_csharp" style="color: inherit; text-decoration: inherit;">Slug</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="description_go">
<a href="#description_go" style="color: inherit; text-decoration: inherit;">Description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}the team's description.
{{% /md %}}</dd><dt class="property-"
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
        <span id="members_go">
<a href="#members_go" style="color: inherit; text-decoration: inherit;">Members</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}List of team members
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_go">
<a href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}the team's full name.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="nodeid_go">
<a href="#nodeid_go" style="color: inherit; text-decoration: inherit;">Node<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}the Node ID of the team.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="permission_go">
<a href="#permission_go" style="color: inherit; text-decoration: inherit;">Permission</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}the team's permission level.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="privacy_go">
<a href="#privacy_go" style="color: inherit; text-decoration: inherit;">Privacy</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}the team's privacy type.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="repositories_go">
<a href="#repositories_go" style="color: inherit; text-decoration: inherit;">Repositories</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}List of team repositories
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="slug_go">
<a href="#slug_go" style="color: inherit; text-decoration: inherit;">Slug</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="description_nodejs">
<a href="#description_nodejs" style="color: inherit; text-decoration: inherit;">description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}the team's description.
{{% /md %}}</dd><dt class="property-"
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
        <span id="members_nodejs">
<a href="#members_nodejs" style="color: inherit; text-decoration: inherit;">members</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}List of team members
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_nodejs">
<a href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}the team's full name.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="nodeid_nodejs">
<a href="#nodeid_nodejs" style="color: inherit; text-decoration: inherit;">node<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}the Node ID of the team.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="permission_nodejs">
<a href="#permission_nodejs" style="color: inherit; text-decoration: inherit;">permission</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}the team's permission level.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="privacy_nodejs">
<a href="#privacy_nodejs" style="color: inherit; text-decoration: inherit;">privacy</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}the team's privacy type.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="repositories_nodejs">
<a href="#repositories_nodejs" style="color: inherit; text-decoration: inherit;">repositories</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}List of team repositories
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="slug_nodejs">
<a href="#slug_nodejs" style="color: inherit; text-decoration: inherit;">slug</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="description_python">
<a href="#description_python" style="color: inherit; text-decoration: inherit;">description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}the team's description.
{{% /md %}}</dd><dt class="property-"
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
        <span id="members_python">
<a href="#members_python" style="color: inherit; text-decoration: inherit;">members</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}List of team members
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_python">
<a href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}the team's full name.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="node_id_python">
<a href="#node_id_python" style="color: inherit; text-decoration: inherit;">node_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}the Node ID of the team.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="permission_python">
<a href="#permission_python" style="color: inherit; text-decoration: inherit;">permission</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}the team's permission level.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="privacy_python">
<a href="#privacy_python" style="color: inherit; text-decoration: inherit;">privacy</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}the team's privacy type.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="repositories_python">
<a href="#repositories_python" style="color: inherit; text-decoration: inherit;">repositories</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}List of team repositories
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="slug_python">
<a href="#slug_python" style="color: inherit; text-decoration: inherit;">slug</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}





<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-github">https://github.com/pulumi/pulumi-github</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
	<dt>Notes</dt>
	<dd>{{% md %}}This Pulumi package is based on the [`github` Terraform Provider](https://github.com/terraform-providers/terraform-provider-github).{{% /md %}}</dd>
</dl>
