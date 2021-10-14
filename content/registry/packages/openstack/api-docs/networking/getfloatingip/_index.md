
---
title: "getFloatingIp"
title_tag: "openstack.networking.getFloatingIp"
meta_desc: "Documentation for the openstack.networking.getFloatingIp function with examples, input properties, output properties, and supporting types."
layout: api
no_edit_this_page: true
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Use this data source to get the ID of an available OpenStack floating IP.


{{% examples %}}

## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}





{{< example csharp >}}

```csharp
using Pulumi;
using OpenStack = Pulumi.OpenStack;

class MyStack : Stack
{
    public MyStack()
    {
        var floatingip1 = Output.Create(OpenStack.Networking.GetFloatingIp.InvokeAsync(new OpenStack.Networking.GetFloatingIpArgs
        {
            Address = "192.168.0.4",
        }));
    }

}
```


{{< /example >}}


{{< example go >}}

```go
package main

import (
	"github.com/pulumi/pulumi-openstack/sdk/v3/go/openstack/networking"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		opt0 := "192.168.0.4"
		_, err := networking.LookupFloatingIp(ctx, &networking.LookupFloatingIpArgs{
			Address: &opt0,
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
import pulumi_openstack as openstack

floatingip1 = openstack.networking.get_floating_ip(address="192.168.0.4")
```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as openstack from "@pulumi/openstack";

const floatingip1 = pulumi.output(openstack.networking.getFloatingIp({
    address: "192.168.0.4",
}, { async: true }));
```


{{< /example >}}





{{% /examples %}}




## Using getFloatingIp {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getFloatingIp<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetFloatingIpArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetFloatingIpResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>get_floating_ip(</span><span class="nx">address</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                    <span class="nx">description</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                    <span class="nx">fixed_ip</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                    <span class="nx">pool</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                    <span class="nx">port_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                    <span class="nx">region</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                    <span class="nx">status</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                    <span class="nx">tags</span><span class="p">:</span> <span class="nx">Optional[Sequence[str]]</span> = None<span class="p">,</span>
                    <span class="nx">tenant_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                    <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> GetFloatingIpResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>LookupFloatingIp<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">args</span><span class="p"> *</span><span class="nx">LookupFloatingIpArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">LookupFloatingIpResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `LookupFloatingIp` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetFloatingIp </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetFloatingIpResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">GetFloatingIpArgs</span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="address_csharp">
<a href="#address_csharp" style="color: inherit; text-decoration: inherit;">Address</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The IP address of the floating IP.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="description_csharp">
<a href="#description_csharp" style="color: inherit; text-decoration: inherit;">Description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Human-readable description of the floating IP.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="fixedip_csharp">
<a href="#fixedip_csharp" style="color: inherit; text-decoration: inherit;">Fixed<wbr>Ip</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The specific IP address of the internal port which should be associated with the floating IP.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="pool_csharp">
<a href="#pool_csharp" style="color: inherit; text-decoration: inherit;">Pool</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the pool from which the floating IP belongs to.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="portid_csharp">
<a href="#portid_csharp" style="color: inherit; text-decoration: inherit;">Port<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the port the floating IP is attached.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="region_csharp">
<a href="#region_csharp" style="color: inherit; text-decoration: inherit;">Region</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The region in which to obtain the V2 Neutron client.
A Neutron client is needed to retrieve floating IP ids. If omitted, the
`region` argument of the provider is used.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="status_csharp">
<a href="#status_csharp" style="color: inherit; text-decoration: inherit;">Status</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}status of the floating IP (ACTIVE/DOWN).
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="tags_csharp">
<a href="#tags_csharp" style="color: inherit; text-decoration: inherit;">Tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}The list of floating IP tags to filter.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="tenantid_csharp">
<a href="#tenantid_csharp" style="color: inherit; text-decoration: inherit;">Tenant<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The owner of the floating IP.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="address_go">
<a href="#address_go" style="color: inherit; text-decoration: inherit;">Address</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The IP address of the floating IP.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="description_go">
<a href="#description_go" style="color: inherit; text-decoration: inherit;">Description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Human-readable description of the floating IP.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="fixedip_go">
<a href="#fixedip_go" style="color: inherit; text-decoration: inherit;">Fixed<wbr>Ip</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The specific IP address of the internal port which should be associated with the floating IP.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="pool_go">
<a href="#pool_go" style="color: inherit; text-decoration: inherit;">Pool</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the pool from which the floating IP belongs to.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="portid_go">
<a href="#portid_go" style="color: inherit; text-decoration: inherit;">Port<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the port the floating IP is attached.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="region_go">
<a href="#region_go" style="color: inherit; text-decoration: inherit;">Region</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The region in which to obtain the V2 Neutron client.
A Neutron client is needed to retrieve floating IP ids. If omitted, the
`region` argument of the provider is used.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="status_go">
<a href="#status_go" style="color: inherit; text-decoration: inherit;">Status</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}status of the floating IP (ACTIVE/DOWN).
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="tags_go">
<a href="#tags_go" style="color: inherit; text-decoration: inherit;">Tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}The list of floating IP tags to filter.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="tenantid_go">
<a href="#tenantid_go" style="color: inherit; text-decoration: inherit;">Tenant<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The owner of the floating IP.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="address_nodejs">
<a href="#address_nodejs" style="color: inherit; text-decoration: inherit;">address</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The IP address of the floating IP.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="description_nodejs">
<a href="#description_nodejs" style="color: inherit; text-decoration: inherit;">description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Human-readable description of the floating IP.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="fixedip_nodejs">
<a href="#fixedip_nodejs" style="color: inherit; text-decoration: inherit;">fixed<wbr>Ip</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The specific IP address of the internal port which should be associated with the floating IP.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="pool_nodejs">
<a href="#pool_nodejs" style="color: inherit; text-decoration: inherit;">pool</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the pool from which the floating IP belongs to.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="portid_nodejs">
<a href="#portid_nodejs" style="color: inherit; text-decoration: inherit;">port<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the port the floating IP is attached.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="region_nodejs">
<a href="#region_nodejs" style="color: inherit; text-decoration: inherit;">region</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The region in which to obtain the V2 Neutron client.
A Neutron client is needed to retrieve floating IP ids. If omitted, the
`region` argument of the provider is used.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="status_nodejs">
<a href="#status_nodejs" style="color: inherit; text-decoration: inherit;">status</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}status of the floating IP (ACTIVE/DOWN).
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="tags_nodejs">
<a href="#tags_nodejs" style="color: inherit; text-decoration: inherit;">tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}The list of floating IP tags to filter.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="tenantid_nodejs">
<a href="#tenantid_nodejs" style="color: inherit; text-decoration: inherit;">tenant<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The owner of the floating IP.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="address_python">
<a href="#address_python" style="color: inherit; text-decoration: inherit;">address</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The IP address of the floating IP.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="description_python">
<a href="#description_python" style="color: inherit; text-decoration: inherit;">description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Human-readable description of the floating IP.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="fixed_ip_python">
<a href="#fixed_ip_python" style="color: inherit; text-decoration: inherit;">fixed_<wbr>ip</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The specific IP address of the internal port which should be associated with the floating IP.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="pool_python">
<a href="#pool_python" style="color: inherit; text-decoration: inherit;">pool</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the pool from which the floating IP belongs to.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="port_id_python">
<a href="#port_id_python" style="color: inherit; text-decoration: inherit;">port_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the port the floating IP is attached.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="region_python">
<a href="#region_python" style="color: inherit; text-decoration: inherit;">region</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The region in which to obtain the V2 Neutron client.
A Neutron client is needed to retrieve floating IP ids. If omitted, the
`region` argument of the provider is used.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="status_python">
<a href="#status_python" style="color: inherit; text-decoration: inherit;">status</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}status of the floating IP (ACTIVE/DOWN).
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="tags_python">
<a href="#tags_python" style="color: inherit; text-decoration: inherit;">tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}The list of floating IP tags to filter.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="tenant_id_python">
<a href="#tenant_id_python" style="color: inherit; text-decoration: inherit;">tenant_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The owner of the floating IP.
{{% /md %}}</dd></dl>
{{% /choosable %}}




## getFloatingIp Result {#result}

The following output properties are available:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="alltags_csharp">
<a href="#alltags_csharp" style="color: inherit; text-decoration: inherit;">All<wbr>Tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}A set of string tags applied on the floating IP.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="dnsdomain_csharp">
<a href="#dnsdomain_csharp" style="color: inherit; text-decoration: inherit;">Dns<wbr>Domain</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The floating IP DNS domain. Available, when Neutron DNS
extension is enabled.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="dnsname_csharp">
<a href="#dnsname_csharp" style="color: inherit; text-decoration: inherit;">Dns<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The floating IP DNS name. Available, when Neutron DNS extension
is enabled.
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
        <span id="address_csharp">
<a href="#address_csharp" style="color: inherit; text-decoration: inherit;">Address</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="description_csharp">
<a href="#description_csharp" style="color: inherit; text-decoration: inherit;">Description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="fixedip_csharp">
<a href="#fixedip_csharp" style="color: inherit; text-decoration: inherit;">Fixed<wbr>Ip</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="pool_csharp">
<a href="#pool_csharp" style="color: inherit; text-decoration: inherit;">Pool</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="portid_csharp">
<a href="#portid_csharp" style="color: inherit; text-decoration: inherit;">Port<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="region_csharp">
<a href="#region_csharp" style="color: inherit; text-decoration: inherit;">Region</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="status_csharp">
<a href="#status_csharp" style="color: inherit; text-decoration: inherit;">Status</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="tags_csharp">
<a href="#tags_csharp" style="color: inherit; text-decoration: inherit;">Tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="tenantid_csharp">
<a href="#tenantid_csharp" style="color: inherit; text-decoration: inherit;">Tenant<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="alltags_go">
<a href="#alltags_go" style="color: inherit; text-decoration: inherit;">All<wbr>Tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A set of string tags applied on the floating IP.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="dnsdomain_go">
<a href="#dnsdomain_go" style="color: inherit; text-decoration: inherit;">Dns<wbr>Domain</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The floating IP DNS domain. Available, when Neutron DNS
extension is enabled.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="dnsname_go">
<a href="#dnsname_go" style="color: inherit; text-decoration: inherit;">Dns<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The floating IP DNS name. Available, when Neutron DNS extension
is enabled.
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
        <span id="address_go">
<a href="#address_go" style="color: inherit; text-decoration: inherit;">Address</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="description_go">
<a href="#description_go" style="color: inherit; text-decoration: inherit;">Description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="fixedip_go">
<a href="#fixedip_go" style="color: inherit; text-decoration: inherit;">Fixed<wbr>Ip</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="pool_go">
<a href="#pool_go" style="color: inherit; text-decoration: inherit;">Pool</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="portid_go">
<a href="#portid_go" style="color: inherit; text-decoration: inherit;">Port<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="region_go">
<a href="#region_go" style="color: inherit; text-decoration: inherit;">Region</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="status_go">
<a href="#status_go" style="color: inherit; text-decoration: inherit;">Status</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="tags_go">
<a href="#tags_go" style="color: inherit; text-decoration: inherit;">Tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="tenantid_go">
<a href="#tenantid_go" style="color: inherit; text-decoration: inherit;">Tenant<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="alltags_nodejs">
<a href="#alltags_nodejs" style="color: inherit; text-decoration: inherit;">all<wbr>Tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}A set of string tags applied on the floating IP.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="dnsdomain_nodejs">
<a href="#dnsdomain_nodejs" style="color: inherit; text-decoration: inherit;">dns<wbr>Domain</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The floating IP DNS domain. Available, when Neutron DNS
extension is enabled.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="dnsname_nodejs">
<a href="#dnsname_nodejs" style="color: inherit; text-decoration: inherit;">dns<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The floating IP DNS name. Available, when Neutron DNS extension
is enabled.
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
        <span id="address_nodejs">
<a href="#address_nodejs" style="color: inherit; text-decoration: inherit;">address</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="description_nodejs">
<a href="#description_nodejs" style="color: inherit; text-decoration: inherit;">description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="fixedip_nodejs">
<a href="#fixedip_nodejs" style="color: inherit; text-decoration: inherit;">fixed<wbr>Ip</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="pool_nodejs">
<a href="#pool_nodejs" style="color: inherit; text-decoration: inherit;">pool</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="portid_nodejs">
<a href="#portid_nodejs" style="color: inherit; text-decoration: inherit;">port<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="region_nodejs">
<a href="#region_nodejs" style="color: inherit; text-decoration: inherit;">region</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="status_nodejs">
<a href="#status_nodejs" style="color: inherit; text-decoration: inherit;">status</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="tags_nodejs">
<a href="#tags_nodejs" style="color: inherit; text-decoration: inherit;">tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="tenantid_nodejs">
<a href="#tenantid_nodejs" style="color: inherit; text-decoration: inherit;">tenant<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="all_tags_python">
<a href="#all_tags_python" style="color: inherit; text-decoration: inherit;">all_<wbr>tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}A set of string tags applied on the floating IP.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="dns_domain_python">
<a href="#dns_domain_python" style="color: inherit; text-decoration: inherit;">dns_<wbr>domain</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The floating IP DNS domain. Available, when Neutron DNS
extension is enabled.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="dns_name_python">
<a href="#dns_name_python" style="color: inherit; text-decoration: inherit;">dns_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The floating IP DNS name. Available, when Neutron DNS extension
is enabled.
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
        <span id="address_python">
<a href="#address_python" style="color: inherit; text-decoration: inherit;">address</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="description_python">
<a href="#description_python" style="color: inherit; text-decoration: inherit;">description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="fixed_ip_python">
<a href="#fixed_ip_python" style="color: inherit; text-decoration: inherit;">fixed_<wbr>ip</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="pool_python">
<a href="#pool_python" style="color: inherit; text-decoration: inherit;">pool</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="port_id_python">
<a href="#port_id_python" style="color: inherit; text-decoration: inherit;">port_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="region_python">
<a href="#region_python" style="color: inherit; text-decoration: inherit;">region</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="status_python">
<a href="#status_python" style="color: inherit; text-decoration: inherit;">status</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="tags_python">
<a href="#tags_python" style="color: inherit; text-decoration: inherit;">tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="tenant_id_python">
<a href="#tenant_id_python" style="color: inherit; text-decoration: inherit;">tenant_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
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
