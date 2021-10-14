
---
title: "Route"
title_tag: "azure-native.network.Route"
meta_desc: "Documentation for the azure-native.network.Route resource with examples, input properties, output properties, lookup functions, and supporting types."
layout: api
no_edit_this_page: true
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Route resource.
API Version: 2020-11-01.

{{% examples %}}

## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}


### Create route


{{< example csharp >}}

```csharp
using Pulumi;
using AzureNative = Pulumi.AzureNative;

class MyStack : Stack
{
    public MyStack()
    {
        var route = new AzureNative.Network.Route("route", new AzureNative.Network.RouteArgs
        {
            AddressPrefix = "10.0.3.0/24",
            NextHopType = "VirtualNetworkGateway",
            ResourceGroupName = "rg1",
            RouteName = "route1",
            RouteTableName = "testrt",
        });
    }

}

```


{{< /example >}}


{{< example go >}}


```go
package main

import (
	network "github.com/pulumi/pulumi-azure-native/sdk/go/azure/network"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		_, err := network.NewRoute(ctx, "route", &network.RouteArgs{
			AddressPrefix:     pulumi.String("10.0.3.0/24"),
			NextHopType:       pulumi.String("VirtualNetworkGateway"),
			ResourceGroupName: pulumi.String("rg1"),
			RouteName:         pulumi.String("route1"),
			RouteTableName:    pulumi.String("testrt"),
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
import pulumi_azure_native as azure_native

route = azure_native.network.Route("route",
    address_prefix="10.0.3.0/24",
    next_hop_type="VirtualNetworkGateway",
    resource_group_name="rg1",
    route_name="route1",
    route_table_name="testrt")

```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as azure_native from "@pulumi/azure-native";

const route = new azure_native.network.Route("route", {
    addressPrefix: "10.0.3.0/24",
    nextHopType: "VirtualNetworkGateway",
    resourceGroupName: "rg1",
    routeName: "route1",
    routeTableName: "testrt",
});

```


{{< /example >}}





{{% /examples %}}




## Create a Route Resource {#create}
{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx">Route</span><span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">RouteArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class=nd>@overload</span>
<span class="k">def </span><span class="nx">Route</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
          <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">,</span>
          <span class="nx">address_prefix</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
          <span class="nx">has_bgp_override</span><span class="p">:</span> <span class="nx">Optional[bool]</span> = None<span class="p">,</span>
          <span class="nx">id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
          <span class="nx">name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
          <span class="nx">next_hop_ip_address</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
          <span class="nx">next_hop_type</span><span class="p">:</span> <span class="nx">Optional[Union[str, RouteNextHopType]]</span> = None<span class="p">,</span>
          <span class="nx">resource_group_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
          <span class="nx">route_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
          <span class="nx">route_table_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
          <span class="nx">type</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">)</span>
<span class=nd>@overload</span>
<span class="k">def </span><span class="nx">Route</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
          <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">RouteInitArgs</a></span><span class="p">,</span>
          <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span><span class="nx">NewRoute</span><span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">name</span><span class="p"> </span><span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p"> </span><span class="nx"><a href="#inputs">RouteArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx">Route</span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx">Route</span><span class="p">(</span><span class="nx">string</span><span class="p"> </span><span class="nx">name<span class="p">,</span> <span class="nx"><a href="#inputs">RouteArgs</a></span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span class="property-type"><a href="#inputs">RouteArgs</a></span>
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
        <span class="property-type"><a href="#inputs">RouteInitArgs</a></span>
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
        <span class="property-type"><a href="#inputs">RouteArgs</a></span>
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
        <span class="property-type"><a href="#inputs">RouteArgs</a></span>
    </dt>
    <dd>The arguments to resource properties.</dd><dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>
    </dt>
    <dd>Bag of options to control resource&#39;s behavior.</dd></dl>

{{% /choosable %}}

## Route Resource Properties {#properties}

To learn more about resource properties and how to use them, see [Inputs and Outputs]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) in the Architecture and Concepts docs.

### Inputs

The Route resource accepts the following [input]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) properties:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="nexthoptype_csharp">
<a href="#nexthoptype_csharp" style="color: inherit; text-decoration: inherit;">Next<wbr>Hop<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string | <a href="#routenexthoptype">Pulumi.<wbr>Azure<wbr>Native.<wbr>Network.<wbr>Route<wbr>Next<wbr>Hop<wbr>Type</a></span>
    </dt>
    <dd>{{% md %}}The type of Azure hop the packet should be sent to.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resourcegroupname_csharp">
<a href="#resourcegroupname_csharp" style="color: inherit; text-decoration: inherit;">Resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource group.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="routetablename_csharp">
<a href="#routetablename_csharp" style="color: inherit; text-decoration: inherit;">Route<wbr>Table<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the route table.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="addressprefix_csharp">
<a href="#addressprefix_csharp" style="color: inherit; text-decoration: inherit;">Address<wbr>Prefix</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The destination CIDR to which the route applies.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="hasbgpoverride_csharp">
<a href="#hasbgpoverride_csharp" style="color: inherit; text-decoration: inherit;">Has<wbr>Bgp<wbr>Override</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}A value indicating whether this route overrides overlapping BGP routes regardless of LPM.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="id_csharp">
<a href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource ID.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource that is unique within a resource group. This name can be used to access the resource.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="nexthopipaddress_csharp">
<a href="#nexthopipaddress_csharp" style="color: inherit; text-decoration: inherit;">Next<wbr>Hop<wbr>Ip<wbr>Address</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The IP address packets should be forwarded to. Next hop values are only allowed in routes where the next hop type is VirtualAppliance.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="routename_csharp">
<a href="#routename_csharp" style="color: inherit; text-decoration: inherit;">Route<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the route.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="type_csharp">
<a href="#type_csharp" style="color: inherit; text-decoration: inherit;">Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of the resource.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="nexthoptype_go">
<a href="#nexthoptype_go" style="color: inherit; text-decoration: inherit;">Next<wbr>Hop<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string | <a href="#routenexthoptype">Route<wbr>Next<wbr>Hop<wbr>Type</a></span>
    </dt>
    <dd>{{% md %}}The type of Azure hop the packet should be sent to.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resourcegroupname_go">
<a href="#resourcegroupname_go" style="color: inherit; text-decoration: inherit;">Resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource group.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="routetablename_go">
<a href="#routetablename_go" style="color: inherit; text-decoration: inherit;">Route<wbr>Table<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the route table.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="addressprefix_go">
<a href="#addressprefix_go" style="color: inherit; text-decoration: inherit;">Address<wbr>Prefix</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The destination CIDR to which the route applies.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="hasbgpoverride_go">
<a href="#hasbgpoverride_go" style="color: inherit; text-decoration: inherit;">Has<wbr>Bgp<wbr>Override</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}A value indicating whether this route overrides overlapping BGP routes regardless of LPM.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="id_go">
<a href="#id_go" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource ID.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="name_go">
<a href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource that is unique within a resource group. This name can be used to access the resource.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="nexthopipaddress_go">
<a href="#nexthopipaddress_go" style="color: inherit; text-decoration: inherit;">Next<wbr>Hop<wbr>Ip<wbr>Address</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The IP address packets should be forwarded to. Next hop values are only allowed in routes where the next hop type is VirtualAppliance.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="routename_go">
<a href="#routename_go" style="color: inherit; text-decoration: inherit;">Route<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the route.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="type_go">
<a href="#type_go" style="color: inherit; text-decoration: inherit;">Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of the resource.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="nexthoptype_nodejs">
<a href="#nexthoptype_nodejs" style="color: inherit; text-decoration: inherit;">next<wbr>Hop<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string | <a href="#routenexthoptype">Route<wbr>Next<wbr>Hop<wbr>Type</a></span>
    </dt>
    <dd>{{% md %}}The type of Azure hop the packet should be sent to.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resourcegroupname_nodejs">
<a href="#resourcegroupname_nodejs" style="color: inherit; text-decoration: inherit;">resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource group.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="routetablename_nodejs">
<a href="#routetablename_nodejs" style="color: inherit; text-decoration: inherit;">route<wbr>Table<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the route table.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="addressprefix_nodejs">
<a href="#addressprefix_nodejs" style="color: inherit; text-decoration: inherit;">address<wbr>Prefix</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The destination CIDR to which the route applies.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="hasbgpoverride_nodejs">
<a href="#hasbgpoverride_nodejs" style="color: inherit; text-decoration: inherit;">has<wbr>Bgp<wbr>Override</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}A value indicating whether this route overrides overlapping BGP routes regardless of LPM.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="id_nodejs">
<a href="#id_nodejs" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource ID.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="name_nodejs">
<a href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource that is unique within a resource group. This name can be used to access the resource.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="nexthopipaddress_nodejs">
<a href="#nexthopipaddress_nodejs" style="color: inherit; text-decoration: inherit;">next<wbr>Hop<wbr>Ip<wbr>Address</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The IP address packets should be forwarded to. Next hop values are only allowed in routes where the next hop type is VirtualAppliance.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="routename_nodejs">
<a href="#routename_nodejs" style="color: inherit; text-decoration: inherit;">route<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the route.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="type_nodejs">
<a href="#type_nodejs" style="color: inherit; text-decoration: inherit;">type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of the resource.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="next_hop_type_python">
<a href="#next_hop_type_python" style="color: inherit; text-decoration: inherit;">next_<wbr>hop_<wbr>type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str | <a href="#routenexthoptype">Route<wbr>Next<wbr>Hop<wbr>Type</a></span>
    </dt>
    <dd>{{% md %}}The type of Azure hop the packet should be sent to.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resource_group_name_python">
<a href="#resource_group_name_python" style="color: inherit; text-decoration: inherit;">resource_<wbr>group_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the resource group.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="route_table_name_python">
<a href="#route_table_name_python" style="color: inherit; text-decoration: inherit;">route_<wbr>table_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the route table.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="address_prefix_python">
<a href="#address_prefix_python" style="color: inherit; text-decoration: inherit;">address_<wbr>prefix</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The destination CIDR to which the route applies.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="has_bgp_override_python">
<a href="#has_bgp_override_python" style="color: inherit; text-decoration: inherit;">has_<wbr>bgp_<wbr>override</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}A value indicating whether this route overrides overlapping BGP routes regardless of LPM.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="id_python">
<a href="#id_python" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Resource ID.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="name_python">
<a href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the resource that is unique within a resource group. This name can be used to access the resource.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="next_hop_ip_address_python">
<a href="#next_hop_ip_address_python" style="color: inherit; text-decoration: inherit;">next_<wbr>hop_<wbr>ip_<wbr>address</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The IP address packets should be forwarded to. Next hop values are only allowed in routes where the next hop type is VirtualAppliance.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="route_name_python">
<a href="#route_name_python" style="color: inherit; text-decoration: inherit;">route_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the route.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="type_python">
<a href="#type_python" style="color: inherit; text-decoration: inherit;">type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The type of the resource.{{% /md %}}</dd></dl>
{{% /choosable %}}


### Outputs

All [input](#inputs) properties are implicitly available as output properties. Additionally, the Route resource produces the following output properties:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="etag_csharp">
<a href="#etag_csharp" style="color: inherit; text-decoration: inherit;">Etag</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A unique read-only string that changes whenever the resource is updated.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_csharp">
<a href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="provisioningstate_csharp">
<a href="#provisioningstate_csharp" style="color: inherit; text-decoration: inherit;">Provisioning<wbr>State</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provisioning state of the route resource.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="etag_go">
<a href="#etag_go" style="color: inherit; text-decoration: inherit;">Etag</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A unique read-only string that changes whenever the resource is updated.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_go">
<a href="#id_go" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="provisioningstate_go">
<a href="#provisioningstate_go" style="color: inherit; text-decoration: inherit;">Provisioning<wbr>State</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provisioning state of the route resource.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="etag_nodejs">
<a href="#etag_nodejs" style="color: inherit; text-decoration: inherit;">etag</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A unique read-only string that changes whenever the resource is updated.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_nodejs">
<a href="#id_nodejs" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="provisioningstate_nodejs">
<a href="#provisioningstate_nodejs" style="color: inherit; text-decoration: inherit;">provisioning<wbr>State</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provisioning state of the route resource.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="etag_python">
<a href="#etag_python" style="color: inherit; text-decoration: inherit;">etag</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A unique read-only string that changes whenever the resource is updated.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_python">
<a href="#id_python" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="provisioning_state_python">
<a href="#provisioning_state_python" style="color: inherit; text-decoration: inherit;">provisioning_<wbr>state</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The provisioning state of the route resource.{{% /md %}}</dd></dl>
{{% /choosable %}}







## Supporting Types



<h4 id="routenexthoptype">Route<wbr>Next<wbr>Hop<wbr>Type</h4>

{{% choosable language csharp %}}
<dl class="tabular"><dt>Virtual<wbr>Network<wbr>Gateway</dt>
    <dd>VirtualNetworkGateway</dd><dt>Vnet<wbr>Local</dt>
    <dd>VnetLocal</dd><dt>Internet</dt>
    <dd>Internet</dd><dt>Virtual<wbr>Appliance</dt>
    <dd>VirtualAppliance</dd><dt>None</dt>
    <dd>None</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="tabular"><dt>Route<wbr>Next<wbr>Hop<wbr>Type<wbr>Virtual<wbr>Network<wbr>Gateway</dt>
    <dd>VirtualNetworkGateway</dd><dt>Route<wbr>Next<wbr>Hop<wbr>Type<wbr>Vnet<wbr>Local</dt>
    <dd>VnetLocal</dd><dt>Route<wbr>Next<wbr>Hop<wbr>Type<wbr>Internet</dt>
    <dd>Internet</dd><dt>Route<wbr>Next<wbr>Hop<wbr>Type<wbr>Virtual<wbr>Appliance</dt>
    <dd>VirtualAppliance</dd><dt>Route<wbr>Next<wbr>Hop<wbr>Type<wbr>None</dt>
    <dd>None</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="tabular"><dt>Virtual<wbr>Network<wbr>Gateway</dt>
    <dd>VirtualNetworkGateway</dd><dt>Vnet<wbr>Local</dt>
    <dd>VnetLocal</dd><dt>Internet</dt>
    <dd>Internet</dd><dt>Virtual<wbr>Appliance</dt>
    <dd>VirtualAppliance</dd><dt>None</dt>
    <dd>None</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="tabular"><dt>VIRTUAL_NETWORK_GATEWAY</dt>
    <dd>VirtualNetworkGateway</dd><dt>VNET_LOCAL</dt>
    <dd>VnetLocal</dd><dt>INTERNET</dt>
    <dd>Internet</dd><dt>VIRTUAL_APPLIANCE</dt>
    <dd>VirtualAppliance</dd><dt>NONE</dt>
    <dd>None</dd></dl>
{{% /choosable %}}
## Import


An existing resource can be imported using its type token, name, and identifier, e.g.

```sh
$ pulumi import azure-native:network:Route route1 /subscriptions/subid/resourceGroups/rg1/providers/Microsoft.Network/routeTables/testrt/routes/route1 
```




<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-azure-native">https://github.com/pulumi/pulumi-azure-native</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
</dl>
