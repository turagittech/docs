
---
title: "getTlsPrivateKey"
title_tag: "fastly.getTlsPrivateKey"
meta_desc: "Documentation for the fastly.getTlsPrivateKey function with examples, input properties, output properties, and supporting types."
layout: api
no_edit_this_page: true
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Use this data source to get information on a TLS Private Key uploaded to Fastly.

> **Warning:** The data source's filters are applied using an **AND** boolean operator, so depending on the combination
 of filters, they may become mutually exclusive. The exception to this is `id` which must not be specified in combination
 with any of the others.

> **Note:** If more or less than a single match is returned by the search, this provider will fail. Ensure that your search
 is specific enough to return a single key.


{{% examples %}}

## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}





{{< example csharp >}}

```csharp
using Pulumi;
using Fastly = Pulumi.Fastly;

class MyStack : Stack
{
    public MyStack()
    {
        var demo = Output.Create(Fastly.GetTlsPrivateKey.InvokeAsync(new Fastly.GetTlsPrivateKeyArgs
        {
            Name = "demo-private-key",
        }));
        this.PrivateKeyNeedsReplacing = demo.Apply(demo => demo.Replace);
    }

    [Output("privateKeyNeedsReplacing")]
    public Output<string> PrivateKeyNeedsReplacing { get; set; }
}
```


{{< /example >}}


{{< example go >}}

```go
package main

import (
	"github.com/pulumi/pulumi-fastly/sdk/v3/go/fastly"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		opt0 := "demo-private-key"
		demo, err := fastly.LookupTlsPrivateKey(ctx, &fastly.LookupTlsPrivateKeyArgs{
			Name: &opt0,
		}, nil)
		if err != nil {
			return err
		}
		ctx.Export("privateKeyNeedsReplacing", demo.Replace)
		return nil
	})
}
```


{{< /example >}}


{{< example python >}}

```python
import pulumi
import pulumi_fastly as fastly

demo = fastly.get_tls_private_key(name="demo-private-key")
pulumi.export("privateKeyNeedsReplacing", demo.replace)
```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as fastly from "@pulumi/fastly";

const demo = fastly.getTlsPrivateKey({
    name: "demo-private-key",
});
export const privateKeyNeedsReplacing = demo.then(demo => demo.replace);
```


{{< /example >}}





{{% /examples %}}




## Using getTlsPrivateKey {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getTlsPrivateKey<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetTlsPrivateKeyArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetTlsPrivateKeyResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>get_tls_private_key(</span><span class="nx">created_at</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                        <span class="nx">id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                        <span class="nx">key_length</span><span class="p">:</span> <span class="nx">Optional[int]</span> = None<span class="p">,</span>
                        <span class="nx">key_type</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                        <span class="nx">name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                        <span class="nx">public_key_sha1</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                        <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> GetTlsPrivateKeyResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>LookupTlsPrivateKey<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">args</span><span class="p"> *</span><span class="nx">LookupTlsPrivateKeyArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">LookupTlsPrivateKeyResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `LookupTlsPrivateKey` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetTlsPrivateKey </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetTlsPrivateKeyResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">GetTlsPrivateKeyArgs</span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="createdat_csharp">
<a href="#createdat_csharp" style="color: inherit; text-decoration: inherit;">Created<wbr>At</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Timestamp (GMT) when the private key was created.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="id_csharp">
<a href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Fastly private key ID. Conflicts with all the other filters
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="keylength_csharp">
<a href="#keylength_csharp" style="color: inherit; text-decoration: inherit;">Key<wbr>Length</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The key length used to generate the private key.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="keytype_csharp">
<a href="#keytype_csharp" style="color: inherit; text-decoration: inherit;">Key<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The algorithm used to generate the private key. Must be RSA.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The human-readable name assigned to the private key when uploaded.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="publickeysha1_csharp">
<a href="#publickeysha1_csharp" style="color: inherit; text-decoration: inherit;">Public<wbr>Key<wbr>Sha1</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A hash of the associated public key, useful for safely identifying it.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="createdat_go">
<a href="#createdat_go" style="color: inherit; text-decoration: inherit;">Created<wbr>At</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Timestamp (GMT) when the private key was created.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="id_go">
<a href="#id_go" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Fastly private key ID. Conflicts with all the other filters
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="keylength_go">
<a href="#keylength_go" style="color: inherit; text-decoration: inherit;">Key<wbr>Length</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The key length used to generate the private key.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="keytype_go">
<a href="#keytype_go" style="color: inherit; text-decoration: inherit;">Key<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The algorithm used to generate the private key. Must be RSA.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="name_go">
<a href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The human-readable name assigned to the private key when uploaded.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="publickeysha1_go">
<a href="#publickeysha1_go" style="color: inherit; text-decoration: inherit;">Public<wbr>Key<wbr>Sha1</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A hash of the associated public key, useful for safely identifying it.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="createdat_nodejs">
<a href="#createdat_nodejs" style="color: inherit; text-decoration: inherit;">created<wbr>At</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Timestamp (GMT) when the private key was created.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="id_nodejs">
<a href="#id_nodejs" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Fastly private key ID. Conflicts with all the other filters
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="keylength_nodejs">
<a href="#keylength_nodejs" style="color: inherit; text-decoration: inherit;">key<wbr>Length</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The key length used to generate the private key.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="keytype_nodejs">
<a href="#keytype_nodejs" style="color: inherit; text-decoration: inherit;">key<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The algorithm used to generate the private key. Must be RSA.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="name_nodejs">
<a href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The human-readable name assigned to the private key when uploaded.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="publickeysha1_nodejs">
<a href="#publickeysha1_nodejs" style="color: inherit; text-decoration: inherit;">public<wbr>Key<wbr>Sha1</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A hash of the associated public key, useful for safely identifying it.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="created_at_python">
<a href="#created_at_python" style="color: inherit; text-decoration: inherit;">created_<wbr>at</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Timestamp (GMT) when the private key was created.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="id_python">
<a href="#id_python" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Fastly private key ID. Conflicts with all the other filters
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="key_length_python">
<a href="#key_length_python" style="color: inherit; text-decoration: inherit;">key_<wbr>length</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The key length used to generate the private key.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="key_type_python">
<a href="#key_type_python" style="color: inherit; text-decoration: inherit;">key_<wbr>type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The algorithm used to generate the private key. Must be RSA.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="name_python">
<a href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The human-readable name assigned to the private key when uploaded.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="public_key_sha1_python">
<a href="#public_key_sha1_python" style="color: inherit; text-decoration: inherit;">public_<wbr>key_<wbr>sha1</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A hash of the associated public key, useful for safely identifying it.
{{% /md %}}</dd></dl>
{{% /choosable %}}




## getTlsPrivateKey Result {#result}

The following output properties are available:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="createdat_csharp">
<a href="#createdat_csharp" style="color: inherit; text-decoration: inherit;">Created<wbr>At</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Timestamp (GMT) when the private key was created.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_csharp">
<a href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Fastly private key ID. Conflicts with all the other filters
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="keylength_csharp">
<a href="#keylength_csharp" style="color: inherit; text-decoration: inherit;">Key<wbr>Length</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The key length used to generate the private key.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="keytype_csharp">
<a href="#keytype_csharp" style="color: inherit; text-decoration: inherit;">Key<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The algorithm used to generate the private key. Must be RSA.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The human-readable name assigned to the private key when uploaded.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="publickeysha1_csharp">
<a href="#publickeysha1_csharp" style="color: inherit; text-decoration: inherit;">Public<wbr>Key<wbr>Sha1</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A hash of the associated public key, useful for safely identifying it.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="replace_csharp">
<a href="#replace_csharp" style="color: inherit; text-decoration: inherit;">Replace</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether Fastly recommends replacing this private key.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="createdat_go">
<a href="#createdat_go" style="color: inherit; text-decoration: inherit;">Created<wbr>At</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Timestamp (GMT) when the private key was created.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_go">
<a href="#id_go" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Fastly private key ID. Conflicts with all the other filters
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="keylength_go">
<a href="#keylength_go" style="color: inherit; text-decoration: inherit;">Key<wbr>Length</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The key length used to generate the private key.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="keytype_go">
<a href="#keytype_go" style="color: inherit; text-decoration: inherit;">Key<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The algorithm used to generate the private key. Must be RSA.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_go">
<a href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The human-readable name assigned to the private key when uploaded.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="publickeysha1_go">
<a href="#publickeysha1_go" style="color: inherit; text-decoration: inherit;">Public<wbr>Key<wbr>Sha1</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A hash of the associated public key, useful for safely identifying it.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="replace_go">
<a href="#replace_go" style="color: inherit; text-decoration: inherit;">Replace</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether Fastly recommends replacing this private key.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="createdat_nodejs">
<a href="#createdat_nodejs" style="color: inherit; text-decoration: inherit;">created<wbr>At</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Timestamp (GMT) when the private key was created.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_nodejs">
<a href="#id_nodejs" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Fastly private key ID. Conflicts with all the other filters
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="keylength_nodejs">
<a href="#keylength_nodejs" style="color: inherit; text-decoration: inherit;">key<wbr>Length</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The key length used to generate the private key.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="keytype_nodejs">
<a href="#keytype_nodejs" style="color: inherit; text-decoration: inherit;">key<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The algorithm used to generate the private key. Must be RSA.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_nodejs">
<a href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The human-readable name assigned to the private key when uploaded.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="publickeysha1_nodejs">
<a href="#publickeysha1_nodejs" style="color: inherit; text-decoration: inherit;">public<wbr>Key<wbr>Sha1</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A hash of the associated public key, useful for safely identifying it.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="replace_nodejs">
<a href="#replace_nodejs" style="color: inherit; text-decoration: inherit;">replace</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Whether Fastly recommends replacing this private key.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="created_at_python">
<a href="#created_at_python" style="color: inherit; text-decoration: inherit;">created_<wbr>at</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Timestamp (GMT) when the private key was created.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_python">
<a href="#id_python" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Fastly private key ID. Conflicts with all the other filters
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="key_length_python">
<a href="#key_length_python" style="color: inherit; text-decoration: inherit;">key_<wbr>length</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The key length used to generate the private key.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="key_type_python">
<a href="#key_type_python" style="color: inherit; text-decoration: inherit;">key_<wbr>type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The algorithm used to generate the private key. Must be RSA.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_python">
<a href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The human-readable name assigned to the private key when uploaded.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="public_key_sha1_python">
<a href="#public_key_sha1_python" style="color: inherit; text-decoration: inherit;">public_<wbr>key_<wbr>sha1</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A hash of the associated public key, useful for safely identifying it.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="replace_python">
<a href="#replace_python" style="color: inherit; text-decoration: inherit;">replace</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether Fastly recommends replacing this private key.
{{% /md %}}</dd></dl>
{{% /choosable %}}





<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-fastly">https://github.com/pulumi/pulumi-fastly</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
	<dt>Notes</dt>
	<dd>{{% md %}}This Pulumi package is based on the [`fastly` Terraform Provider](https://github.com/fastly/terraform-provider-fastly).{{% /md %}}</dd>
</dl>
