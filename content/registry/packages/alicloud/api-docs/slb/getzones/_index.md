
---
title: "getZones"
title_tag: "alicloud.slb.getZones"
meta_desc: "Documentation for the alicloud.slb.getZones function with examples, input properties, output properties, and supporting types."
layout: api
no_edit_this_page: true
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

This data source provides availability zones for SLB that can be accessed by an Alibaba Cloud account within the region configured in the provider.

> **NOTE:** Available in v1.73.0+.


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
        var zonesIds = Output.Create(AliCloud.Slb.GetZones.InvokeAsync());
    }

}
```


{{< /example >}}


{{< example go >}}

```go
package main

import (
	"github.com/pulumi/pulumi-alicloud/sdk/v3/go/alicloud/slb"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		_, err := slb.GetZones(ctx, nil, nil)
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

zones_ids = alicloud.slb.get_zones()
```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as alicloud from "@pulumi/alicloud";

// Declare the data source
const zonesIds = pulumi.output(alicloud.slb.getZones({ async: true }));
```


{{< /example >}}





{{% /examples %}}




## Using getZones {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getZones<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetZonesArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetZonesResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>get_zones(</span><span class="nx">available_slb_address_ip_version</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
              <span class="nx">available_slb_address_type</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
              <span class="nx">enable_details</span><span class="p">:</span> <span class="nx">Optional[bool]</span> = None<span class="p">,</span>
              <span class="nx">output_file</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
              <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> GetZonesResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetZones<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">args</span><span class="p"> *</span><span class="nx">GetZonesArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">GetZonesResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `GetZones` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetZones </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetZonesResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">GetZonesArgs</span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="availableslbaddressipversion_csharp">
<a href="#availableslbaddressipversion_csharp" style="color: inherit; text-decoration: inherit;">Available<wbr>Slb<wbr>Address<wbr>Ip<wbr>Version</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Filter the results by a slb instance address version. Can be either `ipv4`, or `ipv6`.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="availableslbaddresstype_csharp">
<a href="#availableslbaddresstype_csharp" style="color: inherit; text-decoration: inherit;">Available<wbr>Slb<wbr>Address<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Filter the results by a slb instance address type. Can be either `Vpc`, `classic_internet` or `classic_intranet`
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="enabledetails_csharp">
<a href="#enabledetails_csharp" style="color: inherit; text-decoration: inherit;">Enable<wbr>Details</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Default to false and only output `id` in the `zones` block. Set it to true can output more details.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="outputfile_csharp">
<a href="#outputfile_csharp" style="color: inherit; text-decoration: inherit;">Output<wbr>File</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="availableslbaddressipversion_go">
<a href="#availableslbaddressipversion_go" style="color: inherit; text-decoration: inherit;">Available<wbr>Slb<wbr>Address<wbr>Ip<wbr>Version</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Filter the results by a slb instance address version. Can be either `ipv4`, or `ipv6`.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="availableslbaddresstype_go">
<a href="#availableslbaddresstype_go" style="color: inherit; text-decoration: inherit;">Available<wbr>Slb<wbr>Address<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Filter the results by a slb instance address type. Can be either `Vpc`, `classic_internet` or `classic_intranet`
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="enabledetails_go">
<a href="#enabledetails_go" style="color: inherit; text-decoration: inherit;">Enable<wbr>Details</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Default to false and only output `id` in the `zones` block. Set it to true can output more details.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="outputfile_go">
<a href="#outputfile_go" style="color: inherit; text-decoration: inherit;">Output<wbr>File</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="availableslbaddressipversion_nodejs">
<a href="#availableslbaddressipversion_nodejs" style="color: inherit; text-decoration: inherit;">available<wbr>Slb<wbr>Address<wbr>Ip<wbr>Version</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Filter the results by a slb instance address version. Can be either `ipv4`, or `ipv6`.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="availableslbaddresstype_nodejs">
<a href="#availableslbaddresstype_nodejs" style="color: inherit; text-decoration: inherit;">available<wbr>Slb<wbr>Address<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Filter the results by a slb instance address type. Can be either `Vpc`, `classic_internet` or `classic_intranet`
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="enabledetails_nodejs">
<a href="#enabledetails_nodejs" style="color: inherit; text-decoration: inherit;">enable<wbr>Details</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Default to false and only output `id` in the `zones` block. Set it to true can output more details.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="outputfile_nodejs">
<a href="#outputfile_nodejs" style="color: inherit; text-decoration: inherit;">output<wbr>File</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="available_slb_address_ip_version_python">
<a href="#available_slb_address_ip_version_python" style="color: inherit; text-decoration: inherit;">available_<wbr>slb_<wbr>address_<wbr>ip_<wbr>version</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Filter the results by a slb instance address version. Can be either `ipv4`, or `ipv6`.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="available_slb_address_type_python">
<a href="#available_slb_address_type_python" style="color: inherit; text-decoration: inherit;">available_<wbr>slb_<wbr>address_<wbr>type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Filter the results by a slb instance address type. Can be either `Vpc`, `classic_internet` or `classic_intranet`
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="enable_details_python">
<a href="#enable_details_python" style="color: inherit; text-decoration: inherit;">enable_<wbr>details</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Default to false and only output `id` in the `zones` block. Set it to true can output more details.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="output_file_python">
<a href="#output_file_python" style="color: inherit; text-decoration: inherit;">output_<wbr>file</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}




## getZones Result {#result}

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
        <span id="ids_csharp">
<a href="#ids_csharp" style="color: inherit; text-decoration: inherit;">Ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}A list of zone IDs.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="zones_csharp">
<a href="#zones_csharp" style="color: inherit; text-decoration: inherit;">Zones</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getzoneszone">List&lt;Pulumi.<wbr>Ali<wbr>Cloud.<wbr>Slb.<wbr>Outputs.<wbr>Get<wbr>Zones<wbr>Zone&gt;</a></span>
    </dt>
    <dd>{{% md %}}A list of availability zones. Each element contains the following attributes:
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="availableslbaddressipversion_csharp">
<a href="#availableslbaddressipversion_csharp" style="color: inherit; text-decoration: inherit;">Available<wbr>Slb<wbr>Address<wbr>Ip<wbr>Version</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="availableslbaddresstype_csharp">
<a href="#availableslbaddresstype_csharp" style="color: inherit; text-decoration: inherit;">Available<wbr>Slb<wbr>Address<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="enabledetails_csharp">
<a href="#enabledetails_csharp" style="color: inherit; text-decoration: inherit;">Enable<wbr>Details</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="outputfile_csharp">
<a href="#outputfile_csharp" style="color: inherit; text-decoration: inherit;">Output<wbr>File</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
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
        <span id="ids_go">
<a href="#ids_go" style="color: inherit; text-decoration: inherit;">Ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of zone IDs.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="zones_go">
<a href="#zones_go" style="color: inherit; text-decoration: inherit;">Zones</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getzoneszone">[]Get<wbr>Zones<wbr>Zone</a></span>
    </dt>
    <dd>{{% md %}}A list of availability zones. Each element contains the following attributes:
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="availableslbaddressipversion_go">
<a href="#availableslbaddressipversion_go" style="color: inherit; text-decoration: inherit;">Available<wbr>Slb<wbr>Address<wbr>Ip<wbr>Version</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="availableslbaddresstype_go">
<a href="#availableslbaddresstype_go" style="color: inherit; text-decoration: inherit;">Available<wbr>Slb<wbr>Address<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="enabledetails_go">
<a href="#enabledetails_go" style="color: inherit; text-decoration: inherit;">Enable<wbr>Details</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="outputfile_go">
<a href="#outputfile_go" style="color: inherit; text-decoration: inherit;">Output<wbr>File</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
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
        <span id="ids_nodejs">
<a href="#ids_nodejs" style="color: inherit; text-decoration: inherit;">ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}A list of zone IDs.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="zones_nodejs">
<a href="#zones_nodejs" style="color: inherit; text-decoration: inherit;">zones</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getzoneszone">Get<wbr>Zones<wbr>Zone[]</a></span>
    </dt>
    <dd>{{% md %}}A list of availability zones. Each element contains the following attributes:
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="availableslbaddressipversion_nodejs">
<a href="#availableslbaddressipversion_nodejs" style="color: inherit; text-decoration: inherit;">available<wbr>Slb<wbr>Address<wbr>Ip<wbr>Version</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="availableslbaddresstype_nodejs">
<a href="#availableslbaddresstype_nodejs" style="color: inherit; text-decoration: inherit;">available<wbr>Slb<wbr>Address<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="enabledetails_nodejs">
<a href="#enabledetails_nodejs" style="color: inherit; text-decoration: inherit;">enable<wbr>Details</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="outputfile_nodejs">
<a href="#outputfile_nodejs" style="color: inherit; text-decoration: inherit;">output<wbr>File</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
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
        <span id="ids_python">
<a href="#ids_python" style="color: inherit; text-decoration: inherit;">ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}A list of zone IDs.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="zones_python">
<a href="#zones_python" style="color: inherit; text-decoration: inherit;">zones</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getzoneszone">Sequence[Get<wbr>Zones<wbr>Zone]</a></span>
    </dt>
    <dd>{{% md %}}A list of availability zones. Each element contains the following attributes:
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="available_slb_address_ip_version_python">
<a href="#available_slb_address_ip_version_python" style="color: inherit; text-decoration: inherit;">available_<wbr>slb_<wbr>address_<wbr>ip_<wbr>version</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="available_slb_address_type_python">
<a href="#available_slb_address_type_python" style="color: inherit; text-decoration: inherit;">available_<wbr>slb_<wbr>address_<wbr>type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="enable_details_python">
<a href="#enable_details_python" style="color: inherit; text-decoration: inherit;">enable_<wbr>details</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="output_file_python">
<a href="#output_file_python" style="color: inherit; text-decoration: inherit;">output_<wbr>file</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}




## Supporting Types


<h4 id="getzoneszone">Get<wbr>Zones<wbr>Zone</h4>



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="id_csharp">
<a href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID of the zone.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="slbslavezoneids_csharp">
<a href="#slbslavezoneids_csharp" style="color: inherit; text-decoration: inherit;">Slb<wbr>Slave<wbr>Zone<wbr>Ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}A list of slb slave zone ids in which the slb master zone.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="id_go">
<a href="#id_go" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID of the zone.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="slbslavezoneids_go">
<a href="#slbslavezoneids_go" style="color: inherit; text-decoration: inherit;">Slb<wbr>Slave<wbr>Zone<wbr>Ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of slb slave zone ids in which the slb master zone.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="id_nodejs">
<a href="#id_nodejs" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID of the zone.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="slbslavezoneids_nodejs">
<a href="#slbslavezoneids_nodejs" style="color: inherit; text-decoration: inherit;">slb<wbr>Slave<wbr>Zone<wbr>Ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}A list of slb slave zone ids in which the slb master zone.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="id_python">
<a href="#id_python" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}ID of the zone.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="slb_slave_zone_ids_python">
<a href="#slb_slave_zone_ids_python" style="color: inherit; text-decoration: inherit;">slb_<wbr>slave_<wbr>zone_<wbr>ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}A list of slb slave zone ids in which the slb master zone.
{{% /md %}}</dd></dl>
{{% /choosable %}}





<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-alicloud">https://github.com/pulumi/pulumi-alicloud</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
	<dt>Notes</dt>
	<dd>{{% md %}}This Pulumi package is based on the [`alicloud` Terraform Provider](https://github.com/aliyun/terraform-provider-alicloud).{{% /md %}}</dd>
</dl>
