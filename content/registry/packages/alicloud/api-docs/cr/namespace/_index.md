
---
title: "Namespace"
title_tag: "alicloud.cr.Namespace"
meta_desc: "Documentation for the alicloud.cr.Namespace resource with examples, input properties, output properties, lookup functions, and supporting types."
layout: api
no_edit_this_page: true
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

This resource will help you to manager Container Registry namespaces.

> **NOTE:** Available in v1.34.0+.

> **NOTE:** You need to set your registry password in Container Registry console before use this resource.

{{% examples %}}

## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}





{{< example csharp >}}

```csharp
using Pulumi;
using AliCloud = Pulumi.AliCloud;

class MyStack : Stack
{
    public MyStack()
    {
        var my_namespace = new AliCloud.CR.Namespace("my-namespace", new AliCloud.CR.NamespaceArgs
        {
            AutoCreate = false,
            DefaultVisibility = "PUBLIC",
        });
    }

}
```


{{< /example >}}


{{< example go >}}

```go
package main

import (
	"github.com/pulumi/pulumi-alicloud/sdk/v3/go/alicloud/cr"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		_, err := cr.NewNamespace(ctx, "my_namespace", &cr.NamespaceArgs{
			AutoCreate:        pulumi.Bool(false),
			DefaultVisibility: pulumi.String("PUBLIC"),
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
import pulumi_alicloud as alicloud

my_namespace = alicloud.cr.Namespace("my-namespace",
    auto_create=False,
    default_visibility="PUBLIC")
```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as alicloud from "@pulumi/alicloud";

const my_namespace = new alicloud.cr.Namespace("my-namespace", {
    autoCreate: false,
    defaultVisibility: "PUBLIC",
});
```


{{< /example >}}





{{% /examples %}}




## Create a Namespace Resource {#create}
{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx">Namespace</span><span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">NamespaceArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class=nd>@overload</span>
<span class="k">def </span><span class="nx">Namespace</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
              <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">,</span>
              <span class="nx">auto_create</span><span class="p">:</span> <span class="nx">Optional[bool]</span> = None<span class="p">,</span>
              <span class="nx">default_visibility</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
              <span class="nx">name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">)</span>
<span class=nd>@overload</span>
<span class="k">def </span><span class="nx">Namespace</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
              <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">NamespaceArgs</a></span><span class="p">,</span>
              <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span><span class="nx">NewNamespace</span><span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">name</span><span class="p"> </span><span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p"> </span><span class="nx"><a href="#inputs">NamespaceArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx">Namespace</span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx">Namespace</span><span class="p">(</span><span class="nx">string</span><span class="p"> </span><span class="nx">name<span class="p">,</span> <span class="nx"><a href="#inputs">NamespaceArgs</a></span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language nodejs %}}

<dl class="resources-properties"><dt
        class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>The unique name of the resource.</dd><dt
        class="property-required" title="Required">
        <span>args</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#inputs">NamespaceArgs</a></span>
    </dt>
    <dd>The arguments to resource properties.</dd><dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span>
    </dt>
    <dd>Bag of options to control resource&#39;s behavior.</dd></dl>

{{% /choosable %}}

{{% choosable language python %}}

<dl class="resources-properties"><dt
        class="property-required" title="Required">
        <span>resource_name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>The unique name of the resource.</dd><dt
        class="property-required" title="Required">
        <span>args</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#inputs">NamespaceArgs</a></span>
    </dt>
    <dd>The arguments to resource properties.</dd><dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">ResourceOptions</a></span>
    </dt>
    <dd>Bag of options to control resource&#39;s behavior.</dd></dl>

{{% /choosable %}}

{{% choosable language go %}}

<dl class="resources-properties"><dt
        class="property-optional" title="Optional">
        <span>ctx</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span>
    </dt>
    <dd>Context object for the current deployment.</dd><dt
        class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>The unique name of the resource.</dd><dt
        class="property-required" title="Required">
        <span>args</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#inputs">NamespaceArgs</a></span>
    </dt>
    <dd>The arguments to resource properties.</dd><dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span>
    </dt>
    <dd>Bag of options to control resource&#39;s behavior.</dd></dl>

{{% /choosable %}}

{{% choosable language csharp %}}

<dl class="resources-properties"><dt
        class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>The unique name of the resource.</dd><dt
        class="property-required" title="Required">
        <span>args</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#inputs">NamespaceArgs</a></span>
    </dt>
    <dd>The arguments to resource properties.</dd><dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>
    </dt>
    <dd>Bag of options to control resource&#39;s behavior.</dd></dl>

{{% /choosable %}}

## Namespace Resource Properties {#properties}

To learn more about resource properties and how to use them, see [Inputs and Outputs]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) in the Architecture and Concepts docs.

### Inputs

The Namespace resource accepts the following [input]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) properties:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="autocreate_csharp">
<a href="#autocreate_csharp" style="color: inherit; text-decoration: inherit;">Auto<wbr>Create</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Boolean, when it set to true, repositories are automatically created when pushing new images. If it set to false, you create repository for images before pushing.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="defaultvisibility_csharp">
<a href="#defaultvisibility_csharp" style="color: inherit; text-decoration: inherit;">Default<wbr>Visibility</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}`PUBLIC` or `PRIVATE`, default repository visibility in this namespace.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of Container Registry namespace.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="autocreate_go">
<a href="#autocreate_go" style="color: inherit; text-decoration: inherit;">Auto<wbr>Create</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Boolean, when it set to true, repositories are automatically created when pushing new images. If it set to false, you create repository for images before pushing.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="defaultvisibility_go">
<a href="#defaultvisibility_go" style="color: inherit; text-decoration: inherit;">Default<wbr>Visibility</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}`PUBLIC` or `PRIVATE`, default repository visibility in this namespace.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="name_go">
<a href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of Container Registry namespace.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="autocreate_nodejs">
<a href="#autocreate_nodejs" style="color: inherit; text-decoration: inherit;">auto<wbr>Create</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Boolean, when it set to true, repositories are automatically created when pushing new images. If it set to false, you create repository for images before pushing.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="defaultvisibility_nodejs">
<a href="#defaultvisibility_nodejs" style="color: inherit; text-decoration: inherit;">default<wbr>Visibility</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}`PUBLIC` or `PRIVATE`, default repository visibility in this namespace.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="name_nodejs">
<a href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of Container Registry namespace.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="auto_create_python">
<a href="#auto_create_python" style="color: inherit; text-decoration: inherit;">auto_<wbr>create</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Boolean, when it set to true, repositories are automatically created when pushing new images. If it set to false, you create repository for images before pushing.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="default_visibility_python">
<a href="#default_visibility_python" style="color: inherit; text-decoration: inherit;">default_<wbr>visibility</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}`PUBLIC` or `PRIVATE`, default repository visibility in this namespace.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="name_python">
<a href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Name of Container Registry namespace.
{{% /md %}}</dd></dl>
{{% /choosable %}}


### Outputs

All [input](#inputs) properties are implicitly available as output properties. Additionally, the Namespace resource produces the following output properties:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="id_csharp">
<a href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="id_go">
<a href="#id_go" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="id_nodejs">
<a href="#id_nodejs" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="id_python">
<a href="#id_python" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd></dl>
{{% /choosable %}}



## Look up an Existing Namespace Resource {#look-up}

Get an existing Namespace resource's state with the given name, ID, and optional extra properties used to qualify the lookup.
{{< chooser language "typescript,python,go,csharp" / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">public static </span><span class="nf">get</span><span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">string</span><span class="p">,</span> <span class="nx">id</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#ID">Input&lt;ID&gt;</a></span><span class="p">,</span> <span class="nx">state</span><span class="p">?:</span> <span class="nx">NamespaceState</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">): </span><span class="nx">Namespace</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class=nd>@staticmethod</span>
<span class="k">def </span><span class="nf">get</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
        <span class="nx">id</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
        <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">,</span>
        <span class="nx">auto_create</span><span class="p">:</span> <span class="nx">Optional[bool]</span> = None<span class="p">,</span>
        <span class="nx">default_visibility</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
        <span class="nx">name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">) -&gt;</span> Namespace</code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetNamespace<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">name</span><span class="p"> </span><span class="nx">string</span><span class="p">,</span> <span class="nx">id</span><span class="p"> </span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#IDInput">IDInput</a></span><span class="p">,</span> <span class="nx">state</span><span class="p"> *</span><span class="nx">NamespaceState</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx">Namespace</span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static </span><span class="nx">Namespace</span><span class="nf"> Get</span><span class="p">(</span><span class="nx">string</span><span class="p"> </span><span class="nx">name<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.Input-1.html">Input&lt;string&gt;</a></span><span class="p"> </span><span class="nx">id<span class="p">,</span> <span class="nx">NamespaceState</span><span class="p">? </span><span class="nx">state<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language nodejs %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resulting resource.</dd>
    <dt class="property-required" title="Required">
        <span>id</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The <em>unique</em> provider ID of the resource to lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>state</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>Any extra arguments used during the lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>resource_name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resulting resource.</dd>
    <dt class="property-required" title="Optional">
        <span>id</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The <em>unique</em> provider ID of the resource to lookup.</dd>
</dl>
{{% /choosable %}}

{{% choosable language go %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resulting resource.</dd>
    <dt class="property-required" title="Required">
        <span>id</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The <em>unique</em> provider ID of the resource to lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>state</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>Any extra arguments used during the lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

{{% choosable language csharp %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resulting resource.</dd>
    <dt class="property-required" title="Required">
        <span>id</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The <em>unique</em> provider ID of the resource to lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>state</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>Any extra arguments used during the lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

The following state arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_autocreate_csharp">
<a href="#state_autocreate_csharp" style="color: inherit; text-decoration: inherit;">Auto<wbr>Create</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Boolean, when it set to true, repositories are automatically created when pushing new images. If it set to false, you create repository for images before pushing.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_defaultvisibility_csharp">
<a href="#state_defaultvisibility_csharp" style="color: inherit; text-decoration: inherit;">Default<wbr>Visibility</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}`PUBLIC` or `PRIVATE`, default repository visibility in this namespace.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_name_csharp">
<a href="#state_name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of Container Registry namespace.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_autocreate_go">
<a href="#state_autocreate_go" style="color: inherit; text-decoration: inherit;">Auto<wbr>Create</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Boolean, when it set to true, repositories are automatically created when pushing new images. If it set to false, you create repository for images before pushing.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_defaultvisibility_go">
<a href="#state_defaultvisibility_go" style="color: inherit; text-decoration: inherit;">Default<wbr>Visibility</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}`PUBLIC` or `PRIVATE`, default repository visibility in this namespace.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_name_go">
<a href="#state_name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of Container Registry namespace.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_autocreate_nodejs">
<a href="#state_autocreate_nodejs" style="color: inherit; text-decoration: inherit;">auto<wbr>Create</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Boolean, when it set to true, repositories are automatically created when pushing new images. If it set to false, you create repository for images before pushing.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_defaultvisibility_nodejs">
<a href="#state_defaultvisibility_nodejs" style="color: inherit; text-decoration: inherit;">default<wbr>Visibility</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}`PUBLIC` or `PRIVATE`, default repository visibility in this namespace.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_name_nodejs">
<a href="#state_name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of Container Registry namespace.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_auto_create_python">
<a href="#state_auto_create_python" style="color: inherit; text-decoration: inherit;">auto_<wbr>create</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Boolean, when it set to true, repositories are automatically created when pushing new images. If it set to false, you create repository for images before pushing.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_default_visibility_python">
<a href="#state_default_visibility_python" style="color: inherit; text-decoration: inherit;">default_<wbr>visibility</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}`PUBLIC` or `PRIVATE`, default repository visibility in this namespace.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_name_python">
<a href="#state_name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Name of Container Registry namespace.
{{% /md %}}</dd></dl>
{{% /choosable %}}





## Import


Container Registry namespace can be imported using the namespace, e.g.

```sh
 $ pulumi import alicloud:cr/namespace:Namespace default my-namespace
```




<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-alicloud">https://github.com/pulumi/pulumi-alicloud</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
	<dt>Notes</dt>
	<dd>{{% md %}}This Pulumi package is based on the [`alicloud` Terraform Provider](https://github.com/aliyun/terraform-provider-alicloud).{{% /md %}}</dd>
</dl>
