
---
title: "Exchange"
title_tag: "rabbitmq.Exchange"
meta_desc: "Documentation for the rabbitmq.Exchange resource with examples, input properties, output properties, lookup functions, and supporting types."
layout: api
no_edit_this_page: true
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

The ``rabbitmq.Exchange`` resource creates and manages an exchange.

{{% examples %}}

## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}





{{< example csharp >}}

```csharp
using Pulumi;
using RabbitMQ = Pulumi.RabbitMQ;

class MyStack : Stack
{
    public MyStack()
    {
        var testVHost = new RabbitMQ.VHost("testVHost", new RabbitMQ.VHostArgs
        {
        });
        var guest = new RabbitMQ.Permissions("guest", new RabbitMQ.PermissionsArgs
        {
            Permissions = new RabbitMQ.Inputs.PermissionsPermissionsArgs
            {
                Configure = ".*",
                Read = ".*",
                Write = ".*",
            },
            User = "guest",
            Vhost = testVHost.Name,
        });
        var testExchange = new RabbitMQ.Exchange("testExchange", new RabbitMQ.ExchangeArgs
        {
            Settings = new RabbitMQ.Inputs.ExchangeSettingsArgs
            {
                AutoDelete = true,
                Durable = false,
                Type = "fanout",
            },
            Vhost = guest.Vhost,
        });
    }

}
```


{{< /example >}}


{{< example go >}}

```go
package main

import (
	"github.com/pulumi/pulumi-rabbitmq/sdk/v3/go/rabbitmq"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		testVHost, err := rabbitmq.NewVHost(ctx, "testVHost", nil)
		if err != nil {
			return err
		}
		guest, err := rabbitmq.NewPermissions(ctx, "guest", &rabbitmq.PermissionsArgs{
			Permissions: &rabbitmq.PermissionsPermissionsArgs{
				Configure: pulumi.String(".*"),
				Read:      pulumi.String(".*"),
				Write:     pulumi.String(".*"),
			},
			User:  pulumi.String("guest"),
			Vhost: testVHost.Name,
		})
		if err != nil {
			return err
		}
		_, err = rabbitmq.NewExchange(ctx, "testExchange", &rabbitmq.ExchangeArgs{
			Settings: &rabbitmq.ExchangeSettingsArgs{
				AutoDelete: pulumi.Bool(true),
				Durable:    pulumi.Bool(false),
				Type:       pulumi.String("fanout"),
			},
			Vhost: guest.Vhost,
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
import pulumi_rabbitmq as rabbitmq

test_v_host = rabbitmq.VHost("testVHost")
guest = rabbitmq.Permissions("guest",
    permissions=rabbitmq.PermissionsPermissionsArgs(
        configure=".*",
        read=".*",
        write=".*",
    ),
    user="guest",
    vhost=test_v_host.name)
test_exchange = rabbitmq.Exchange("testExchange",
    settings=rabbitmq.ExchangeSettingsArgs(
        auto_delete=True,
        durable=False,
        type="fanout",
    ),
    vhost=guest.vhost)
```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as rabbitmq from "@pulumi/rabbitmq";

const testVHost = new rabbitmq.VHost("test", {});
const guest = new rabbitmq.Permissions("guest", {
    permissions: {
        configure: ".*",
        read: ".*",
        write: ".*",
    },
    user: "guest",
    vhost: testVHost.name,
});
const testExchange = new rabbitmq.Exchange("test", {
    settings: {
        autoDelete: true,
        durable: false,
        type: "fanout",
    },
    vhost: guest.vhost,
});
```


{{< /example >}}





{{% /examples %}}




## Create a Exchange Resource {#create}
{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx">Exchange</span><span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">ExchangeArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class=nd>@overload</span>
<span class="k">def </span><span class="nx">Exchange</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
             <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">,</span>
             <span class="nx">name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
             <span class="nx">settings</span><span class="p">:</span> <span class="nx">Optional[ExchangeSettingsArgs]</span> = None<span class="p">,</span>
             <span class="nx">vhost</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">)</span>
<span class=nd>@overload</span>
<span class="k">def </span><span class="nx">Exchange</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
             <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">ExchangeArgs</a></span><span class="p">,</span>
             <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span><span class="nx">NewExchange</span><span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">name</span><span class="p"> </span><span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p"> </span><span class="nx"><a href="#inputs">ExchangeArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx">Exchange</span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx">Exchange</span><span class="p">(</span><span class="nx">string</span><span class="p"> </span><span class="nx">name<span class="p">,</span> <span class="nx"><a href="#inputs">ExchangeArgs</a></span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span class="property-type"><a href="#inputs">ExchangeArgs</a></span>
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
        <span class="property-type"><a href="#inputs">ExchangeArgs</a></span>
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
        <span class="property-type"><a href="#inputs">ExchangeArgs</a></span>
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
        <span class="property-type"><a href="#inputs">ExchangeArgs</a></span>
    </dt>
    <dd>The arguments to resource properties.</dd><dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>
    </dt>
    <dd>Bag of options to control resource&#39;s behavior.</dd></dl>

{{% /choosable %}}

## Exchange Resource Properties {#properties}

To learn more about resource properties and how to use them, see [Inputs and Outputs]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) in the Architecture and Concepts docs.

### Inputs

The Exchange resource accepts the following [input]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) properties:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="settings_csharp">
<a href="#settings_csharp" style="color: inherit; text-decoration: inherit;">Settings</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#exchangesettings">Pulumi.<wbr>Rabbit<wbr>MQ.<wbr>Inputs.<wbr>Exchange<wbr>Settings<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}The settings of the exchange. The structure is
described below.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the exchange.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="vhost_csharp">
<a href="#vhost_csharp" style="color: inherit; text-decoration: inherit;">Vhost</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The vhost to create the resource in.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="settings_go">
<a href="#settings_go" style="color: inherit; text-decoration: inherit;">Settings</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#exchangesettings">Exchange<wbr>Settings<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}The settings of the exchange. The structure is
described below.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="name_go">
<a href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the exchange.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="vhost_go">
<a href="#vhost_go" style="color: inherit; text-decoration: inherit;">Vhost</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The vhost to create the resource in.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="settings_nodejs">
<a href="#settings_nodejs" style="color: inherit; text-decoration: inherit;">settings</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#exchangesettings">Exchange<wbr>Settings<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}The settings of the exchange. The structure is
described below.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="name_nodejs">
<a href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the exchange.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="vhost_nodejs">
<a href="#vhost_nodejs" style="color: inherit; text-decoration: inherit;">vhost</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The vhost to create the resource in.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="settings_python">
<a href="#settings_python" style="color: inherit; text-decoration: inherit;">settings</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#exchangesettings">Exchange<wbr>Settings<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}The settings of the exchange. The structure is
described below.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="name_python">
<a href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the exchange.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="vhost_python">
<a href="#vhost_python" style="color: inherit; text-decoration: inherit;">vhost</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The vhost to create the resource in.
{{% /md %}}</dd></dl>
{{% /choosable %}}


### Outputs

All [input](#inputs) properties are implicitly available as output properties. Additionally, the Exchange resource produces the following output properties:



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



## Look up an Existing Exchange Resource {#look-up}

Get an existing Exchange resource's state with the given name, ID, and optional extra properties used to qualify the lookup.
{{< chooser language "typescript,python,go,csharp" / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">public static </span><span class="nf">get</span><span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">string</span><span class="p">,</span> <span class="nx">id</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#ID">Input&lt;ID&gt;</a></span><span class="p">,</span> <span class="nx">state</span><span class="p">?:</span> <span class="nx">ExchangeState</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">): </span><span class="nx">Exchange</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class=nd>@staticmethod</span>
<span class="k">def </span><span class="nf">get</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
        <span class="nx">id</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
        <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">,</span>
        <span class="nx">name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
        <span class="nx">settings</span><span class="p">:</span> <span class="nx">Optional[ExchangeSettingsArgs]</span> = None<span class="p">,</span>
        <span class="nx">vhost</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">) -&gt;</span> Exchange</code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetExchange<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">name</span><span class="p"> </span><span class="nx">string</span><span class="p">,</span> <span class="nx">id</span><span class="p"> </span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#IDInput">IDInput</a></span><span class="p">,</span> <span class="nx">state</span><span class="p"> *</span><span class="nx">ExchangeState</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx">Exchange</span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static </span><span class="nx">Exchange</span><span class="nf"> Get</span><span class="p">(</span><span class="nx">string</span><span class="p"> </span><span class="nx">name<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.Input-1.html">Input&lt;string&gt;</a></span><span class="p"> </span><span class="nx">id<span class="p">,</span> <span class="nx">ExchangeState</span><span class="p">? </span><span class="nx">state<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span id="state_name_csharp">
<a href="#state_name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the exchange.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_settings_csharp">
<a href="#state_settings_csharp" style="color: inherit; text-decoration: inherit;">Settings</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#exchangesettings">Pulumi.<wbr>Rabbit<wbr>MQ.<wbr>Inputs.<wbr>Exchange<wbr>Settings<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}The settings of the exchange. The structure is
described below.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_vhost_csharp">
<a href="#state_vhost_csharp" style="color: inherit; text-decoration: inherit;">Vhost</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The vhost to create the resource in.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_name_go">
<a href="#state_name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the exchange.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_settings_go">
<a href="#state_settings_go" style="color: inherit; text-decoration: inherit;">Settings</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#exchangesettings">Exchange<wbr>Settings<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}The settings of the exchange. The structure is
described below.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_vhost_go">
<a href="#state_vhost_go" style="color: inherit; text-decoration: inherit;">Vhost</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The vhost to create the resource in.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_name_nodejs">
<a href="#state_name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the exchange.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_settings_nodejs">
<a href="#state_settings_nodejs" style="color: inherit; text-decoration: inherit;">settings</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#exchangesettings">Exchange<wbr>Settings<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}The settings of the exchange. The structure is
described below.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_vhost_nodejs">
<a href="#state_vhost_nodejs" style="color: inherit; text-decoration: inherit;">vhost</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The vhost to create the resource in.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_name_python">
<a href="#state_name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the exchange.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_settings_python">
<a href="#state_settings_python" style="color: inherit; text-decoration: inherit;">settings</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#exchangesettings">Exchange<wbr>Settings<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}The settings of the exchange. The structure is
described below.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_vhost_python">
<a href="#state_vhost_python" style="color: inherit; text-decoration: inherit;">vhost</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The vhost to create the resource in.
{{% /md %}}</dd></dl>
{{% /choosable %}}






## Supporting Types



<h4 id="exchangesettings">Exchange<wbr>Settings</h4>

{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="type_csharp">
<a href="#type_csharp" style="color: inherit; text-decoration: inherit;">Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of exchange.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="arguments_csharp">
<a href="#arguments_csharp" style="color: inherit; text-decoration: inherit;">Arguments</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary&lt;string, object&gt;</span>
    </dt>
    <dd>{{% md %}}Additional key/value settings for the exchange.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="autodelete_csharp">
<a href="#autodelete_csharp" style="color: inherit; text-decoration: inherit;">Auto<wbr>Delete</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether the exchange will self-delete when all
queues have finished using it.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="durable_csharp">
<a href="#durable_csharp" style="color: inherit; text-decoration: inherit;">Durable</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether the exchange survives server restarts.
Defaults to `false`.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="type_go">
<a href="#type_go" style="color: inherit; text-decoration: inherit;">Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of exchange.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="arguments_go">
<a href="#arguments_go" style="color: inherit; text-decoration: inherit;">Arguments</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}Additional key/value settings for the exchange.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="autodelete_go">
<a href="#autodelete_go" style="color: inherit; text-decoration: inherit;">Auto<wbr>Delete</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether the exchange will self-delete when all
queues have finished using it.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="durable_go">
<a href="#durable_go" style="color: inherit; text-decoration: inherit;">Durable</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether the exchange survives server restarts.
Defaults to `false`.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="type_nodejs">
<a href="#type_nodejs" style="color: inherit; text-decoration: inherit;">type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of exchange.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="arguments_nodejs">
<a href="#arguments_nodejs" style="color: inherit; text-decoration: inherit;">arguments</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}</span>
    </dt>
    <dd>{{% md %}}Additional key/value settings for the exchange.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="autodelete_nodejs">
<a href="#autodelete_nodejs" style="color: inherit; text-decoration: inherit;">auto<wbr>Delete</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Whether the exchange will self-delete when all
queues have finished using it.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="durable_nodejs">
<a href="#durable_nodejs" style="color: inherit; text-decoration: inherit;">durable</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Whether the exchange survives server restarts.
Defaults to `false`.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="type_python">
<a href="#type_python" style="color: inherit; text-decoration: inherit;">type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The type of exchange.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="arguments_python">
<a href="#arguments_python" style="color: inherit; text-decoration: inherit;">arguments</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Mapping[str, Any]</span>
    </dt>
    <dd>{{% md %}}Additional key/value settings for the exchange.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="auto_delete_python">
<a href="#auto_delete_python" style="color: inherit; text-decoration: inherit;">auto_<wbr>delete</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether the exchange will self-delete when all
queues have finished using it.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="durable_python">
<a href="#durable_python" style="color: inherit; text-decoration: inherit;">durable</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether the exchange survives server restarts.
Defaults to `false`.
{{% /md %}}</dd></dl>
{{% /choosable %}}
## Import


Exchanges can be imported using the `id` which is composed of

`name@vhost`. E.g.

```sh
 $ pulumi import rabbitmq:index/exchange:Exchange test test@vhost
```




<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-rabbitmq">https://github.com/pulumi/pulumi-rabbitmq</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
	<dt>Notes</dt>
	<dd>{{% md %}}This Pulumi package is based on the [`rabbitmq` Terraform Provider](https://github.com/terraform-providers/terraform-provider-rabbitmq).{{% /md %}}</dd>
</dl>
