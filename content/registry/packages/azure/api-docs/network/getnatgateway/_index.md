
---
title: "getNatGateway"
title_tag: "azure.network.getNatGateway"
meta_desc: "Documentation for the azure.network.getNatGateway function with examples, input properties, output properties, and supporting types."
layout: api
no_edit_this_page: true
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Use this data source to access information about an existing NAT Gateway.




## Using getNatGateway {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getNatGateway<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetNatGatewayArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetNatGatewayResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>get_nat_gateway(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                    <span class="nx">public_ip_address_ids</span><span class="p">:</span> <span class="nx">Optional[Sequence[str]]</span> = None<span class="p">,</span>
                    <span class="nx">public_ip_prefix_ids</span><span class="p">:</span> <span class="nx">Optional[Sequence[str]]</span> = None<span class="p">,</span>
                    <span class="nx">resource_group_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                    <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> GetNatGatewayResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>LookupNatGateway<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">args</span><span class="p"> *</span><span class="nx">LookupNatGatewayArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">LookupNatGatewayResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `LookupNatGateway` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetNatGateway </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetNatGatewayResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">GetNatGatewayArgs</span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the Name of the NAT Gateway.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resourcegroupname_csharp">
<a href="#resourcegroupname_csharp" style="color: inherit; text-decoration: inherit;">Resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Resource Group where the NAT Gateway exists.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="publicipaddressids_csharp">
<a href="#publicipaddressids_csharp" style="color: inherit; text-decoration: inherit;">Public<wbr>Ip<wbr>Address<wbr>Ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}A list of existing Public IP Address resource IDs which the NAT Gateway is using.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="publicipprefixids_csharp">
<a href="#publicipprefixids_csharp" style="color: inherit; text-decoration: inherit;">Public<wbr>Ip<wbr>Prefix<wbr>Ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}A list of existing Public IP Prefix resource IDs which the NAT Gateway is using.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="name_go">
<a href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the Name of the NAT Gateway.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resourcegroupname_go">
<a href="#resourcegroupname_go" style="color: inherit; text-decoration: inherit;">Resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Resource Group where the NAT Gateway exists.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="publicipaddressids_go">
<a href="#publicipaddressids_go" style="color: inherit; text-decoration: inherit;">Public<wbr>Ip<wbr>Address<wbr>Ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of existing Public IP Address resource IDs which the NAT Gateway is using.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="publicipprefixids_go">
<a href="#publicipprefixids_go" style="color: inherit; text-decoration: inherit;">Public<wbr>Ip<wbr>Prefix<wbr>Ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of existing Public IP Prefix resource IDs which the NAT Gateway is using.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="name_nodejs">
<a href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the Name of the NAT Gateway.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resourcegroupname_nodejs">
<a href="#resourcegroupname_nodejs" style="color: inherit; text-decoration: inherit;">resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Resource Group where the NAT Gateway exists.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="publicipaddressids_nodejs">
<a href="#publicipaddressids_nodejs" style="color: inherit; text-decoration: inherit;">public<wbr>Ip<wbr>Address<wbr>Ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}A list of existing Public IP Address resource IDs which the NAT Gateway is using.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="publicipprefixids_nodejs">
<a href="#publicipprefixids_nodejs" style="color: inherit; text-decoration: inherit;">public<wbr>Ip<wbr>Prefix<wbr>Ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}A list of existing Public IP Prefix resource IDs which the NAT Gateway is using.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="name_python">
<a href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Specifies the Name of the NAT Gateway.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resource_group_name_python">
<a href="#resource_group_name_python" style="color: inherit; text-decoration: inherit;">resource_<wbr>group_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Resource Group where the NAT Gateway exists.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="public_ip_address_ids_python">
<a href="#public_ip_address_ids_python" style="color: inherit; text-decoration: inherit;">public_<wbr>ip_<wbr>address_<wbr>ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}A list of existing Public IP Address resource IDs which the NAT Gateway is using.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="public_ip_prefix_ids_python">
<a href="#public_ip_prefix_ids_python" style="color: inherit; text-decoration: inherit;">public_<wbr>ip_<wbr>prefix_<wbr>ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}A list of existing Public IP Prefix resource IDs which the NAT Gateway is using.
{{% /md %}}</dd></dl>
{{% /choosable %}}




## getNatGateway Result {#result}

The following output properties are available:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
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
        <span id="idletimeoutinminutes_csharp">
<a href="#idletimeoutinminutes_csharp" style="color: inherit; text-decoration: inherit;">Idle<wbr>Timeout<wbr>In<wbr>Minutes</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The idle timeout in minutes which is used for the NAT Gateway.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="location_csharp">
<a href="#location_csharp" style="color: inherit; text-decoration: inherit;">Location</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The location where the NAT Gateway exists.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="publicipaddressids_csharp">
<a href="#publicipaddressids_csharp" style="color: inherit; text-decoration: inherit;">Public<wbr>Ip<wbr>Address<wbr>Ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}A list of existing Public IP Address resource IDs which the NAT Gateway is using.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="publicipprefixids_csharp">
<a href="#publicipprefixids_csharp" style="color: inherit; text-decoration: inherit;">Public<wbr>Ip<wbr>Prefix<wbr>Ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}A list of existing Public IP Prefix resource IDs which the NAT Gateway is using.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="resourcegroupname_csharp">
<a href="#resourcegroupname_csharp" style="color: inherit; text-decoration: inherit;">Resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="resourceguid_csharp">
<a href="#resourceguid_csharp" style="color: inherit; text-decoration: inherit;">Resource<wbr>Guid</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Resource GUID of the NAT Gateway.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="skuname_csharp">
<a href="#skuname_csharp" style="color: inherit; text-decoration: inherit;">Sku<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The SKU used by the NAT Gateway.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="tags_csharp">
<a href="#tags_csharp" style="color: inherit; text-decoration: inherit;">Tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary&lt;string, string&gt;</span>
    </dt>
    <dd>{{% md %}}A mapping of tags assigned to the resource.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="zones_csharp">
<a href="#zones_csharp" style="color: inherit; text-decoration: inherit;">Zones</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}A list of Availability Zones which the NAT Gateway exists in.
{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="idletimeoutinminutes_go">
<a href="#idletimeoutinminutes_go" style="color: inherit; text-decoration: inherit;">Idle<wbr>Timeout<wbr>In<wbr>Minutes</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The idle timeout in minutes which is used for the NAT Gateway.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="location_go">
<a href="#location_go" style="color: inherit; text-decoration: inherit;">Location</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The location where the NAT Gateway exists.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_go">
<a href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="publicipaddressids_go">
<a href="#publicipaddressids_go" style="color: inherit; text-decoration: inherit;">Public<wbr>Ip<wbr>Address<wbr>Ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of existing Public IP Address resource IDs which the NAT Gateway is using.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="publicipprefixids_go">
<a href="#publicipprefixids_go" style="color: inherit; text-decoration: inherit;">Public<wbr>Ip<wbr>Prefix<wbr>Ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of existing Public IP Prefix resource IDs which the NAT Gateway is using.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="resourcegroupname_go">
<a href="#resourcegroupname_go" style="color: inherit; text-decoration: inherit;">Resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="resourceguid_go">
<a href="#resourceguid_go" style="color: inherit; text-decoration: inherit;">Resource<wbr>Guid</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Resource GUID of the NAT Gateway.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="skuname_go">
<a href="#skuname_go" style="color: inherit; text-decoration: inherit;">Sku<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The SKU used by the NAT Gateway.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="tags_go">
<a href="#tags_go" style="color: inherit; text-decoration: inherit;">Tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]string</span>
    </dt>
    <dd>{{% md %}}A mapping of tags assigned to the resource.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="zones_go">
<a href="#zones_go" style="color: inherit; text-decoration: inherit;">Zones</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of Availability Zones which the NAT Gateway exists in.
{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="idletimeoutinminutes_nodejs">
<a href="#idletimeoutinminutes_nodejs" style="color: inherit; text-decoration: inherit;">idle<wbr>Timeout<wbr>In<wbr>Minutes</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The idle timeout in minutes which is used for the NAT Gateway.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="location_nodejs">
<a href="#location_nodejs" style="color: inherit; text-decoration: inherit;">location</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The location where the NAT Gateway exists.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_nodejs">
<a href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="publicipaddressids_nodejs">
<a href="#publicipaddressids_nodejs" style="color: inherit; text-decoration: inherit;">public<wbr>Ip<wbr>Address<wbr>Ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}A list of existing Public IP Address resource IDs which the NAT Gateway is using.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="publicipprefixids_nodejs">
<a href="#publicipprefixids_nodejs" style="color: inherit; text-decoration: inherit;">public<wbr>Ip<wbr>Prefix<wbr>Ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}A list of existing Public IP Prefix resource IDs which the NAT Gateway is using.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="resourcegroupname_nodejs">
<a href="#resourcegroupname_nodejs" style="color: inherit; text-decoration: inherit;">resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="resourceguid_nodejs">
<a href="#resourceguid_nodejs" style="color: inherit; text-decoration: inherit;">resource<wbr>Guid</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Resource GUID of the NAT Gateway.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="skuname_nodejs">
<a href="#skuname_nodejs" style="color: inherit; text-decoration: inherit;">sku<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The SKU used by the NAT Gateway.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="tags_nodejs">
<a href="#tags_nodejs" style="color: inherit; text-decoration: inherit;">tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: string}</span>
    </dt>
    <dd>{{% md %}}A mapping of tags assigned to the resource.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="zones_nodejs">
<a href="#zones_nodejs" style="color: inherit; text-decoration: inherit;">zones</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}A list of Availability Zones which the NAT Gateway exists in.
{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="idle_timeout_in_minutes_python">
<a href="#idle_timeout_in_minutes_python" style="color: inherit; text-decoration: inherit;">idle_<wbr>timeout_<wbr>in_<wbr>minutes</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The idle timeout in minutes which is used for the NAT Gateway.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="location_python">
<a href="#location_python" style="color: inherit; text-decoration: inherit;">location</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The location where the NAT Gateway exists.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_python">
<a href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="public_ip_address_ids_python">
<a href="#public_ip_address_ids_python" style="color: inherit; text-decoration: inherit;">public_<wbr>ip_<wbr>address_<wbr>ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}A list of existing Public IP Address resource IDs which the NAT Gateway is using.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="public_ip_prefix_ids_python">
<a href="#public_ip_prefix_ids_python" style="color: inherit; text-decoration: inherit;">public_<wbr>ip_<wbr>prefix_<wbr>ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}A list of existing Public IP Prefix resource IDs which the NAT Gateway is using.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="resource_group_name_python">
<a href="#resource_group_name_python" style="color: inherit; text-decoration: inherit;">resource_<wbr>group_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="resource_guid_python">
<a href="#resource_guid_python" style="color: inherit; text-decoration: inherit;">resource_<wbr>guid</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The Resource GUID of the NAT Gateway.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="sku_name_python">
<a href="#sku_name_python" style="color: inherit; text-decoration: inherit;">sku_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The SKU used by the NAT Gateway.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="tags_python">
<a href="#tags_python" style="color: inherit; text-decoration: inherit;">tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Mapping[str, str]</span>
    </dt>
    <dd>{{% md %}}A mapping of tags assigned to the resource.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="zones_python">
<a href="#zones_python" style="color: inherit; text-decoration: inherit;">zones</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}A list of Availability Zones which the NAT Gateway exists in.
{{% /md %}}</dd></dl>
{{% /choosable %}}





<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-azure">https://github.com/pulumi/pulumi-azure</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
	<dt>Notes</dt>
	<dd>{{% md %}}This Pulumi package is based on the [`azurerm` Terraform Provider](https://github.com/hashicorp/terraform-provider-azurerm).{{% /md %}}</dd>
</dl>
