
---
title: "PortSecGroupAssociate"
title_tag: "openstack.networking.PortSecGroupAssociate"
meta_desc: "Documentation for the openstack.networking.PortSecGroupAssociate resource with examples, input properties, output properties, lookup functions, and supporting types."
layout: api
no_edit_this_page: true
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->




## Create a PortSecGroupAssociate Resource {#create}
{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx">PortSecGroupAssociate</span><span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">PortSecGroupAssociateArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class=nd>@overload</span>
<span class="k">def </span><span class="nx">PortSecGroupAssociate</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
                          <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">,</span>
                          <span class="nx">enforce</span><span class="p">:</span> <span class="nx">Optional[bool]</span> = None<span class="p">,</span>
                          <span class="nx">port_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                          <span class="nx">region</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                          <span class="nx">security_group_ids</span><span class="p">:</span> <span class="nx">Optional[Sequence[str]]</span> = None<span class="p">)</span>
<span class=nd>@overload</span>
<span class="k">def </span><span class="nx">PortSecGroupAssociate</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
                          <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">PortSecGroupAssociateArgs</a></span><span class="p">,</span>
                          <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span><span class="nx">NewPortSecGroupAssociate</span><span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">name</span><span class="p"> </span><span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p"> </span><span class="nx"><a href="#inputs">PortSecGroupAssociateArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx">PortSecGroupAssociate</span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx">PortSecGroupAssociate</span><span class="p">(</span><span class="nx">string</span><span class="p"> </span><span class="nx">name<span class="p">,</span> <span class="nx"><a href="#inputs">PortSecGroupAssociateArgs</a></span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span class="property-type"><a href="#inputs">PortSecGroupAssociateArgs</a></span>
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
        <span class="property-type"><a href="#inputs">PortSecGroupAssociateArgs</a></span>
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
        <span class="property-type"><a href="#inputs">PortSecGroupAssociateArgs</a></span>
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
        <span class="property-type"><a href="#inputs">PortSecGroupAssociateArgs</a></span>
    </dt>
    <dd>The arguments to resource properties.</dd><dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>
    </dt>
    <dd>Bag of options to control resource&#39;s behavior.</dd></dl>

{{% /choosable %}}

## PortSecGroupAssociate Resource Properties {#properties}

To learn more about resource properties and how to use them, see [Inputs and Outputs]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) in the Architecture and Concepts docs.

### Inputs

The PortSecGroupAssociate resource accepts the following [input]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) properties:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="portid_csharp">
<a href="#portid_csharp" style="color: inherit; text-decoration: inherit;">Port<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}An UUID of the port to apply security groups to.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="securitygroupids_csharp">
<a href="#securitygroupids_csharp" style="color: inherit; text-decoration: inherit;">Security<wbr>Group<wbr>Ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}A list of security group IDs to apply to
the port. The security groups must be specified by ID and not name (as
opposed to how they are configured with the Compute Instance).
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="enforce_csharp">
<a href="#enforce_csharp" style="color: inherit; text-decoration: inherit;">Enforce</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether to replace or append the list of security
groups, specified in the `security_group_ids`. Defaults to `false`.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="region_csharp">
<a href="#region_csharp" style="color: inherit; text-decoration: inherit;">Region</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The region in which to obtain the V2 networking client.
A networking client is needed to manage a port. If omitted, the
`region` argument of the provider is used. Changing this creates a new
resource.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="portid_go">
<a href="#portid_go" style="color: inherit; text-decoration: inherit;">Port<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}An UUID of the port to apply security groups to.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="securitygroupids_go">
<a href="#securitygroupids_go" style="color: inherit; text-decoration: inherit;">Security<wbr>Group<wbr>Ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of security group IDs to apply to
the port. The security groups must be specified by ID and not name (as
opposed to how they are configured with the Compute Instance).
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="enforce_go">
<a href="#enforce_go" style="color: inherit; text-decoration: inherit;">Enforce</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether to replace or append the list of security
groups, specified in the `security_group_ids`. Defaults to `false`.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="region_go">
<a href="#region_go" style="color: inherit; text-decoration: inherit;">Region</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The region in which to obtain the V2 networking client.
A networking client is needed to manage a port. If omitted, the
`region` argument of the provider is used. Changing this creates a new
resource.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="portid_nodejs">
<a href="#portid_nodejs" style="color: inherit; text-decoration: inherit;">port<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}An UUID of the port to apply security groups to.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="securitygroupids_nodejs">
<a href="#securitygroupids_nodejs" style="color: inherit; text-decoration: inherit;">security<wbr>Group<wbr>Ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}A list of security group IDs to apply to
the port. The security groups must be specified by ID and not name (as
opposed to how they are configured with the Compute Instance).
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="enforce_nodejs">
<a href="#enforce_nodejs" style="color: inherit; text-decoration: inherit;">enforce</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Whether to replace or append the list of security
groups, specified in the `security_group_ids`. Defaults to `false`.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="region_nodejs">
<a href="#region_nodejs" style="color: inherit; text-decoration: inherit;">region</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The region in which to obtain the V2 networking client.
A networking client is needed to manage a port. If omitted, the
`region` argument of the provider is used. Changing this creates a new
resource.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="port_id_python">
<a href="#port_id_python" style="color: inherit; text-decoration: inherit;">port_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}An UUID of the port to apply security groups to.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="security_group_ids_python">
<a href="#security_group_ids_python" style="color: inherit; text-decoration: inherit;">security_<wbr>group_<wbr>ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}A list of security group IDs to apply to
the port. The security groups must be specified by ID and not name (as
opposed to how they are configured with the Compute Instance).
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="enforce_python">
<a href="#enforce_python" style="color: inherit; text-decoration: inherit;">enforce</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether to replace or append the list of security
groups, specified in the `security_group_ids`. Defaults to `false`.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="region_python">
<a href="#region_python" style="color: inherit; text-decoration: inherit;">region</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The region in which to obtain the V2 networking client.
A networking client is needed to manage a port. If omitted, the
`region` argument of the provider is used. Changing this creates a new
resource.
{{% /md %}}</dd></dl>
{{% /choosable %}}


### Outputs

All [input](#inputs) properties are implicitly available as output properties. Additionally, the PortSecGroupAssociate resource produces the following output properties:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="allsecuritygroupids_csharp">
<a href="#allsecuritygroupids_csharp" style="color: inherit; text-decoration: inherit;">All<wbr>Security<wbr>Group<wbr>Ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}The collection of Security Group IDs on the port
which have been explicitly and implicitly added.
{{% /md %}}</dd><dt class="property-"
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
        <span id="allsecuritygroupids_go">
<a href="#allsecuritygroupids_go" style="color: inherit; text-decoration: inherit;">All<wbr>Security<wbr>Group<wbr>Ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}The collection of Security Group IDs on the port
which have been explicitly and implicitly added.
{{% /md %}}</dd><dt class="property-"
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
        <span id="allsecuritygroupids_nodejs">
<a href="#allsecuritygroupids_nodejs" style="color: inherit; text-decoration: inherit;">all<wbr>Security<wbr>Group<wbr>Ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}The collection of Security Group IDs on the port
which have been explicitly and implicitly added.
{{% /md %}}</dd><dt class="property-"
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
        <span id="all_security_group_ids_python">
<a href="#all_security_group_ids_python" style="color: inherit; text-decoration: inherit;">all_<wbr>security_<wbr>group_<wbr>ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}The collection of Security Group IDs on the port
which have been explicitly and implicitly added.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_python">
<a href="#id_python" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd></dl>
{{% /choosable %}}



## Look up an Existing PortSecGroupAssociate Resource {#look-up}

Get an existing PortSecGroupAssociate resource's state with the given name, ID, and optional extra properties used to qualify the lookup.
{{< chooser language "typescript,python,go,csharp" / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">public static </span><span class="nf">get</span><span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">string</span><span class="p">,</span> <span class="nx">id</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#ID">Input&lt;ID&gt;</a></span><span class="p">,</span> <span class="nx">state</span><span class="p">?:</span> <span class="nx">PortSecGroupAssociateState</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">): </span><span class="nx">PortSecGroupAssociate</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class=nd>@staticmethod</span>
<span class="k">def </span><span class="nf">get</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
        <span class="nx">id</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
        <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">,</span>
        <span class="nx">all_security_group_ids</span><span class="p">:</span> <span class="nx">Optional[Sequence[str]]</span> = None<span class="p">,</span>
        <span class="nx">enforce</span><span class="p">:</span> <span class="nx">Optional[bool]</span> = None<span class="p">,</span>
        <span class="nx">port_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
        <span class="nx">region</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
        <span class="nx">security_group_ids</span><span class="p">:</span> <span class="nx">Optional[Sequence[str]]</span> = None<span class="p">) -&gt;</span> PortSecGroupAssociate</code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetPortSecGroupAssociate<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">name</span><span class="p"> </span><span class="nx">string</span><span class="p">,</span> <span class="nx">id</span><span class="p"> </span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#IDInput">IDInput</a></span><span class="p">,</span> <span class="nx">state</span><span class="p"> *</span><span class="nx">PortSecGroupAssociateState</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx">PortSecGroupAssociate</span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static </span><span class="nx">PortSecGroupAssociate</span><span class="nf"> Get</span><span class="p">(</span><span class="nx">string</span><span class="p"> </span><span class="nx">name<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.Input-1.html">Input&lt;string&gt;</a></span><span class="p"> </span><span class="nx">id<span class="p">,</span> <span class="nx">PortSecGroupAssociateState</span><span class="p">? </span><span class="nx">state<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span id="state_allsecuritygroupids_csharp">
<a href="#state_allsecuritygroupids_csharp" style="color: inherit; text-decoration: inherit;">All<wbr>Security<wbr>Group<wbr>Ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}The collection of Security Group IDs on the port
which have been explicitly and implicitly added.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_enforce_csharp">
<a href="#state_enforce_csharp" style="color: inherit; text-decoration: inherit;">Enforce</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether to replace or append the list of security
groups, specified in the `security_group_ids`. Defaults to `false`.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_portid_csharp">
<a href="#state_portid_csharp" style="color: inherit; text-decoration: inherit;">Port<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}An UUID of the port to apply security groups to.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_region_csharp">
<a href="#state_region_csharp" style="color: inherit; text-decoration: inherit;">Region</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The region in which to obtain the V2 networking client.
A networking client is needed to manage a port. If omitted, the
`region` argument of the provider is used. Changing this creates a new
resource.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_securitygroupids_csharp">
<a href="#state_securitygroupids_csharp" style="color: inherit; text-decoration: inherit;">Security<wbr>Group<wbr>Ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}A list of security group IDs to apply to
the port. The security groups must be specified by ID and not name (as
opposed to how they are configured with the Compute Instance).
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_allsecuritygroupids_go">
<a href="#state_allsecuritygroupids_go" style="color: inherit; text-decoration: inherit;">All<wbr>Security<wbr>Group<wbr>Ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}The collection of Security Group IDs on the port
which have been explicitly and implicitly added.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_enforce_go">
<a href="#state_enforce_go" style="color: inherit; text-decoration: inherit;">Enforce</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether to replace or append the list of security
groups, specified in the `security_group_ids`. Defaults to `false`.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_portid_go">
<a href="#state_portid_go" style="color: inherit; text-decoration: inherit;">Port<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}An UUID of the port to apply security groups to.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_region_go">
<a href="#state_region_go" style="color: inherit; text-decoration: inherit;">Region</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The region in which to obtain the V2 networking client.
A networking client is needed to manage a port. If omitted, the
`region` argument of the provider is used. Changing this creates a new
resource.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_securitygroupids_go">
<a href="#state_securitygroupids_go" style="color: inherit; text-decoration: inherit;">Security<wbr>Group<wbr>Ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of security group IDs to apply to
the port. The security groups must be specified by ID and not name (as
opposed to how they are configured with the Compute Instance).
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_allsecuritygroupids_nodejs">
<a href="#state_allsecuritygroupids_nodejs" style="color: inherit; text-decoration: inherit;">all<wbr>Security<wbr>Group<wbr>Ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}The collection of Security Group IDs on the port
which have been explicitly and implicitly added.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_enforce_nodejs">
<a href="#state_enforce_nodejs" style="color: inherit; text-decoration: inherit;">enforce</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Whether to replace or append the list of security
groups, specified in the `security_group_ids`. Defaults to `false`.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_portid_nodejs">
<a href="#state_portid_nodejs" style="color: inherit; text-decoration: inherit;">port<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}An UUID of the port to apply security groups to.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_region_nodejs">
<a href="#state_region_nodejs" style="color: inherit; text-decoration: inherit;">region</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The region in which to obtain the V2 networking client.
A networking client is needed to manage a port. If omitted, the
`region` argument of the provider is used. Changing this creates a new
resource.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_securitygroupids_nodejs">
<a href="#state_securitygroupids_nodejs" style="color: inherit; text-decoration: inherit;">security<wbr>Group<wbr>Ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}A list of security group IDs to apply to
the port. The security groups must be specified by ID and not name (as
opposed to how they are configured with the Compute Instance).
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_all_security_group_ids_python">
<a href="#state_all_security_group_ids_python" style="color: inherit; text-decoration: inherit;">all_<wbr>security_<wbr>group_<wbr>ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}The collection of Security Group IDs on the port
which have been explicitly and implicitly added.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_enforce_python">
<a href="#state_enforce_python" style="color: inherit; text-decoration: inherit;">enforce</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether to replace or append the list of security
groups, specified in the `security_group_ids`. Defaults to `false`.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_port_id_python">
<a href="#state_port_id_python" style="color: inherit; text-decoration: inherit;">port_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}An UUID of the port to apply security groups to.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_region_python">
<a href="#state_region_python" style="color: inherit; text-decoration: inherit;">region</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The region in which to obtain the V2 networking client.
A networking client is needed to manage a port. If omitted, the
`region` argument of the provider is used. Changing this creates a new
resource.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_security_group_ids_python">
<a href="#state_security_group_ids_python" style="color: inherit; text-decoration: inherit;">security_<wbr>group_<wbr>ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}A list of security group IDs to apply to
the port. The security groups must be specified by ID and not name (as
opposed to how they are configured with the Compute Instance).
{{% /md %}}</dd></dl>
{{% /choosable %}}







<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-openstack">https://github.com/pulumi/pulumi-openstack</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
	<dt>Notes</dt>
	<dd>{{% md %}}This Pulumi package is based on the [`openstack` Terraform Provider](https://github.com/terraform-provider-openstack/terraform-provider-openstack).{{% /md %}}</dd>
</dl>
