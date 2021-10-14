
---
title: "getVolumes"
title_tag: "hcloud.getVolumes"
meta_desc: "Documentation for the hcloud.getVolumes function with examples, input properties, output properties, and supporting types."
layout: api
no_edit_this_page: true
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Provides details about multiple Hetzner Cloud volumes.


{{% examples %}}

## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}





{{< example csharp >}}

```csharp
using Pulumi;
using HCloud = Pulumi.HCloud;

class MyStack : Stack
{
    public MyStack()
    {
        var volume_ = Output.Create(HCloud.GetVolumes.InvokeAsync());
        var volume3 = Output.Create(HCloud.GetVolumes.InvokeAsync(new HCloud.GetVolumesArgs
        {
            WithSelector = "key=value",
        }));
    }

}
```


{{< /example >}}


{{< example go >}}

```go
package main

import (
	"github.com/pulumi/pulumi-hcloud/sdk/go/hcloud"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		_, err := hcloud.GetVolumes(ctx, nil, nil)
		if err != nil {
			return err
		}
		opt0 := "key=value"
		_, err = hcloud.GetVolumes(ctx, &hcloud.GetVolumesArgs{
			WithSelector: &opt0,
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
import pulumi_hcloud as hcloud

volume_ = hcloud.get_volumes()
volume3 = hcloud.get_volumes(with_selector="key=value")
```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as hcloud from "@pulumi/hcloud";

const volume_ = pulumi.output(hcloud.getVolumes({ async: true }));
const volume3 = pulumi.output(hcloud.getVolumes({
    withSelector: "key=value",
}, { async: true }));
```


{{< /example >}}





{{% /examples %}}




## Using getVolumes {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getVolumes<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetVolumesArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetVolumesResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>get_volumes(</span><span class="nx">with_selector</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                <span class="nx">with_statuses</span><span class="p">:</span> <span class="nx">Optional[Sequence[str]]</span> = None<span class="p">,</span>
                <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> GetVolumesResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetVolumes<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">args</span><span class="p"> *</span><span class="nx">GetVolumesArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">GetVolumesResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `GetVolumes` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetVolumes </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetVolumesResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">GetVolumesArgs</span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="withselector_csharp">
<a href="#withselector_csharp" style="color: inherit; text-decoration: inherit;">With<wbr>Selector</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}[Label selector](https://docs.hetzner.cloud/#overview-label-selector)
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="withstatuses_csharp">
<a href="#withstatuses_csharp" style="color: inherit; text-decoration: inherit;">With<wbr>Statuses</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}List only volumes with the specified status, could contain `creating` or `available`.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="withselector_go">
<a href="#withselector_go" style="color: inherit; text-decoration: inherit;">With<wbr>Selector</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}[Label selector](https://docs.hetzner.cloud/#overview-label-selector)
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="withstatuses_go">
<a href="#withstatuses_go" style="color: inherit; text-decoration: inherit;">With<wbr>Statuses</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}List only volumes with the specified status, could contain `creating` or `available`.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="withselector_nodejs">
<a href="#withselector_nodejs" style="color: inherit; text-decoration: inherit;">with<wbr>Selector</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}[Label selector](https://docs.hetzner.cloud/#overview-label-selector)
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="withstatuses_nodejs">
<a href="#withstatuses_nodejs" style="color: inherit; text-decoration: inherit;">with<wbr>Statuses</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}List only volumes with the specified status, could contain `creating` or `available`.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="with_selector_python">
<a href="#with_selector_python" style="color: inherit; text-decoration: inherit;">with_<wbr>selector</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}[Label selector](https://docs.hetzner.cloud/#overview-label-selector)
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="with_statuses_python">
<a href="#with_statuses_python" style="color: inherit; text-decoration: inherit;">with_<wbr>statuses</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}List only volumes with the specified status, could contain `creating` or `available`.
{{% /md %}}</dd></dl>
{{% /choosable %}}




## getVolumes Result {#result}

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
        <span id="volumes_csharp">
<a href="#volumes_csharp" style="color: inherit; text-decoration: inherit;">Volumes</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getvolumesvolume">List&lt;Pulumi.<wbr>HCloud.<wbr>Outputs.<wbr>Get<wbr>Volumes<wbr>Volume&gt;</a></span>
    </dt>
    <dd>{{% md %}}(list) List of all matching volumes. See `data.hcloud_volume` for schema.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="withselector_csharp">
<a href="#withselector_csharp" style="color: inherit; text-decoration: inherit;">With<wbr>Selector</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="withstatuses_csharp">
<a href="#withstatuses_csharp" style="color: inherit; text-decoration: inherit;">With<wbr>Statuses</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
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
        <span id="volumes_go">
<a href="#volumes_go" style="color: inherit; text-decoration: inherit;">Volumes</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getvolumesvolume">[]Get<wbr>Volumes<wbr>Volume</a></span>
    </dt>
    <dd>{{% md %}}(list) List of all matching volumes. See `data.hcloud_volume` for schema.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="withselector_go">
<a href="#withselector_go" style="color: inherit; text-decoration: inherit;">With<wbr>Selector</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="withstatuses_go">
<a href="#withstatuses_go" style="color: inherit; text-decoration: inherit;">With<wbr>Statuses</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
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
        <span id="volumes_nodejs">
<a href="#volumes_nodejs" style="color: inherit; text-decoration: inherit;">volumes</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getvolumesvolume">Get<wbr>Volumes<wbr>Volume[]</a></span>
    </dt>
    <dd>{{% md %}}(list) List of all matching volumes. See `data.hcloud_volume` for schema.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="withselector_nodejs">
<a href="#withselector_nodejs" style="color: inherit; text-decoration: inherit;">with<wbr>Selector</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="withstatuses_nodejs">
<a href="#withstatuses_nodejs" style="color: inherit; text-decoration: inherit;">with<wbr>Statuses</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
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
        <span id="volumes_python">
<a href="#volumes_python" style="color: inherit; text-decoration: inherit;">volumes</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getvolumesvolume">Sequence[Get<wbr>Volumes<wbr>Volume]</a></span>
    </dt>
    <dd>{{% md %}}(list) List of all matching volumes. See `data.hcloud_volume` for schema.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="with_selector_python">
<a href="#with_selector_python" style="color: inherit; text-decoration: inherit;">with_<wbr>selector</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="with_statuses_python">
<a href="#with_statuses_python" style="color: inherit; text-decoration: inherit;">with_<wbr>statuses</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}




## Supporting Types


<h4 id="getvolumesvolume">Get<wbr>Volumes<wbr>Volume</h4>



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="deleteprotection_csharp">
<a href="#deleteprotection_csharp" style="color: inherit; text-decoration: inherit;">Delete<wbr>Protection</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="id_csharp">
<a href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="labels_csharp">
<a href="#labels_csharp" style="color: inherit; text-decoration: inherit;">Labels</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary&lt;string, object&gt;</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="linuxdevice_csharp">
<a href="#linuxdevice_csharp" style="color: inherit; text-decoration: inherit;">Linux<wbr>Device</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="size_csharp">
<a href="#size_csharp" style="color: inherit; text-decoration: inherit;">Size</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="location_csharp">
<a href="#location_csharp" style="color: inherit; text-decoration: inherit;">Location</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="serverid_csharp">
<a href="#serverid_csharp" style="color: inherit; text-decoration: inherit;">Server<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="deleteprotection_go">
<a href="#deleteprotection_go" style="color: inherit; text-decoration: inherit;">Delete<wbr>Protection</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="id_go">
<a href="#id_go" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="labels_go">
<a href="#labels_go" style="color: inherit; text-decoration: inherit;">Labels</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="linuxdevice_go">
<a href="#linuxdevice_go" style="color: inherit; text-decoration: inherit;">Linux<wbr>Device</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="name_go">
<a href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="size_go">
<a href="#size_go" style="color: inherit; text-decoration: inherit;">Size</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="location_go">
<a href="#location_go" style="color: inherit; text-decoration: inherit;">Location</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="serverid_go">
<a href="#serverid_go" style="color: inherit; text-decoration: inherit;">Server<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="deleteprotection_nodejs">
<a href="#deleteprotection_nodejs" style="color: inherit; text-decoration: inherit;">delete<wbr>Protection</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="id_nodejs">
<a href="#id_nodejs" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="labels_nodejs">
<a href="#labels_nodejs" style="color: inherit; text-decoration: inherit;">labels</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="linuxdevice_nodejs">
<a href="#linuxdevice_nodejs" style="color: inherit; text-decoration: inherit;">linux<wbr>Device</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="name_nodejs">
<a href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="size_nodejs">
<a href="#size_nodejs" style="color: inherit; text-decoration: inherit;">size</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="location_nodejs">
<a href="#location_nodejs" style="color: inherit; text-decoration: inherit;">location</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="serverid_nodejs">
<a href="#serverid_nodejs" style="color: inherit; text-decoration: inherit;">server<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="delete_protection_python">
<a href="#delete_protection_python" style="color: inherit; text-decoration: inherit;">delete_<wbr>protection</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="id_python">
<a href="#id_python" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="labels_python">
<a href="#labels_python" style="color: inherit; text-decoration: inherit;">labels</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Mapping[str, Any]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="linux_device_python">
<a href="#linux_device_python" style="color: inherit; text-decoration: inherit;">linux_<wbr>device</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="name_python">
<a href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="size_python">
<a href="#size_python" style="color: inherit; text-decoration: inherit;">size</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="location_python">
<a href="#location_python" style="color: inherit; text-decoration: inherit;">location</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="server_id_python">
<a href="#server_id_python" style="color: inherit; text-decoration: inherit;">server_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}





<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-hcloud">https://github.com/pulumi/pulumi-hcloud</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
	<dt>Notes</dt>
	<dd>{{% md %}}This Pulumi package is based on the [`hcloud` Terraform Provider](https://github.com/hetznercloud/terraform-provider-hcloud).{{% /md %}}</dd>
</dl>
