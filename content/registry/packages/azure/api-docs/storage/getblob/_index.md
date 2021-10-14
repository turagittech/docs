
---
title: "getBlob"
title_tag: "azure.storage.getBlob"
meta_desc: "Documentation for the azure.storage.getBlob function with examples, input properties, output properties, and supporting types."
layout: api
no_edit_this_page: true
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Use this data source to access information about an existing Storage Blob.


{{% examples %}}

## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}





{{< example csharp >}}

```csharp
using Pulumi;
using Azure = Pulumi.Azure;

class MyStack : Stack
{
    public MyStack()
    {
        var example = Output.Create(Azure.Storage.GetBlob.InvokeAsync(new Azure.Storage.GetBlobArgs
        {
            Name = "example-blob-name",
            StorageAccountName = "example-storage-account-name",
            StorageContainerName = "example-storage-container-name",
        }));
    }

}
```


{{< /example >}}


{{< example go >}}

```go
package main

import (
	"github.com/pulumi/pulumi-azure/sdk/v4/go/azure/storage"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		_, err := storage.LookupBlob(ctx, &storage.LookupBlobArgs{
			Name:                 "example-blob-name",
			StorageAccountName:   "example-storage-account-name",
			StorageContainerName: "example-storage-container-name",
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
import pulumi_azure as azure

example = azure.storage.get_blob(name="example-blob-name",
    storage_account_name="example-storage-account-name",
    storage_container_name="example-storage-container-name")
```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as azure from "@pulumi/azure";

const example = pulumi.output(azure.storage.getBlob({
    name: "example-blob-name",
    storageAccountName: "example-storage-account-name",
    storageContainerName: "example-storage-container-name",
}));
```


{{< /example >}}





{{% /examples %}}




## Using getBlob {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getBlob<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetBlobArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetBlobResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>get_blob(</span><span class="nx">metadata</span><span class="p">:</span> <span class="nx">Optional[Mapping[str, str]]</span> = None<span class="p">,</span>
             <span class="nx">name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
             <span class="nx">storage_account_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
             <span class="nx">storage_container_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
             <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> GetBlobResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>LookupBlob<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">args</span><span class="p"> *</span><span class="nx">LookupBlobArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">LookupBlobResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `LookupBlob` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetBlob </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetBlobResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">GetBlobArgs</span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
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
    <dd>{{% md %}}The name of the Blob.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="storageaccountname_csharp">
<a href="#storageaccountname_csharp" style="color: inherit; text-decoration: inherit;">Storage<wbr>Account<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the Storage Account where the Container exists.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="storagecontainername_csharp">
<a href="#storagecontainername_csharp" style="color: inherit; text-decoration: inherit;">Storage<wbr>Container<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the Storage Container where the Blob exists.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="metadata_csharp">
<a href="#metadata_csharp" style="color: inherit; text-decoration: inherit;">Metadata</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary&lt;string, string&gt;</span>
    </dt>
    <dd>{{% md %}}A map of custom blob metadata.
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
    <dd>{{% md %}}The name of the Blob.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="storageaccountname_go">
<a href="#storageaccountname_go" style="color: inherit; text-decoration: inherit;">Storage<wbr>Account<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the Storage Account where the Container exists.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="storagecontainername_go">
<a href="#storagecontainername_go" style="color: inherit; text-decoration: inherit;">Storage<wbr>Container<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the Storage Container where the Blob exists.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="metadata_go">
<a href="#metadata_go" style="color: inherit; text-decoration: inherit;">Metadata</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]string</span>
    </dt>
    <dd>{{% md %}}A map of custom blob metadata.
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
    <dd>{{% md %}}The name of the Blob.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="storageaccountname_nodejs">
<a href="#storageaccountname_nodejs" style="color: inherit; text-decoration: inherit;">storage<wbr>Account<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the Storage Account where the Container exists.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="storagecontainername_nodejs">
<a href="#storagecontainername_nodejs" style="color: inherit; text-decoration: inherit;">storage<wbr>Container<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the Storage Container where the Blob exists.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="metadata_nodejs">
<a href="#metadata_nodejs" style="color: inherit; text-decoration: inherit;">metadata</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: string}</span>
    </dt>
    <dd>{{% md %}}A map of custom blob metadata.
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
    <dd>{{% md %}}The name of the Blob.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="storage_account_name_python">
<a href="#storage_account_name_python" style="color: inherit; text-decoration: inherit;">storage_<wbr>account_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the Storage Account where the Container exists.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="storage_container_name_python">
<a href="#storage_container_name_python" style="color: inherit; text-decoration: inherit;">storage_<wbr>container_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the Storage Container where the Blob exists.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="metadata_python">
<a href="#metadata_python" style="color: inherit; text-decoration: inherit;">metadata</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Mapping[str, str]</span>
    </dt>
    <dd>{{% md %}}A map of custom blob metadata.
{{% /md %}}</dd></dl>
{{% /choosable %}}




## getBlob Result {#result}

The following output properties are available:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="accesstier_csharp">
<a href="#accesstier_csharp" style="color: inherit; text-decoration: inherit;">Access<wbr>Tier</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The access tier of the storage blob.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="contentmd5_csharp">
<a href="#contentmd5_csharp" style="color: inherit; text-decoration: inherit;">Content<wbr>Md5</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The MD5 sum of the blob contents.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="contenttype_csharp">
<a href="#contenttype_csharp" style="color: inherit; text-decoration: inherit;">Content<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The content type of the storage blob.
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
        <span id="metadata_csharp">
<a href="#metadata_csharp" style="color: inherit; text-decoration: inherit;">Metadata</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary&lt;string, string&gt;</span>
    </dt>
    <dd>{{% md %}}A map of custom blob metadata.
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
        <span id="storageaccountname_csharp">
<a href="#storageaccountname_csharp" style="color: inherit; text-decoration: inherit;">Storage<wbr>Account<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="storagecontainername_csharp">
<a href="#storagecontainername_csharp" style="color: inherit; text-decoration: inherit;">Storage<wbr>Container<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_csharp">
<a href="#type_csharp" style="color: inherit; text-decoration: inherit;">Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of the storage blob
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="url_csharp">
<a href="#url_csharp" style="color: inherit; text-decoration: inherit;">Url</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The URL of the storage blob.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="accesstier_go">
<a href="#accesstier_go" style="color: inherit; text-decoration: inherit;">Access<wbr>Tier</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The access tier of the storage blob.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="contentmd5_go">
<a href="#contentmd5_go" style="color: inherit; text-decoration: inherit;">Content<wbr>Md5</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The MD5 sum of the blob contents.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="contenttype_go">
<a href="#contenttype_go" style="color: inherit; text-decoration: inherit;">Content<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The content type of the storage blob.
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
        <span id="metadata_go">
<a href="#metadata_go" style="color: inherit; text-decoration: inherit;">Metadata</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]string</span>
    </dt>
    <dd>{{% md %}}A map of custom blob metadata.
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
        <span id="storageaccountname_go">
<a href="#storageaccountname_go" style="color: inherit; text-decoration: inherit;">Storage<wbr>Account<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="storagecontainername_go">
<a href="#storagecontainername_go" style="color: inherit; text-decoration: inherit;">Storage<wbr>Container<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_go">
<a href="#type_go" style="color: inherit; text-decoration: inherit;">Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of the storage blob
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="url_go">
<a href="#url_go" style="color: inherit; text-decoration: inherit;">Url</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The URL of the storage blob.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="accesstier_nodejs">
<a href="#accesstier_nodejs" style="color: inherit; text-decoration: inherit;">access<wbr>Tier</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The access tier of the storage blob.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="contentmd5_nodejs">
<a href="#contentmd5_nodejs" style="color: inherit; text-decoration: inherit;">content<wbr>Md5</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The MD5 sum of the blob contents.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="contenttype_nodejs">
<a href="#contenttype_nodejs" style="color: inherit; text-decoration: inherit;">content<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The content type of the storage blob.
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
        <span id="metadata_nodejs">
<a href="#metadata_nodejs" style="color: inherit; text-decoration: inherit;">metadata</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: string}</span>
    </dt>
    <dd>{{% md %}}A map of custom blob metadata.
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
        <span id="storageaccountname_nodejs">
<a href="#storageaccountname_nodejs" style="color: inherit; text-decoration: inherit;">storage<wbr>Account<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="storagecontainername_nodejs">
<a href="#storagecontainername_nodejs" style="color: inherit; text-decoration: inherit;">storage<wbr>Container<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_nodejs">
<a href="#type_nodejs" style="color: inherit; text-decoration: inherit;">type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of the storage blob
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="url_nodejs">
<a href="#url_nodejs" style="color: inherit; text-decoration: inherit;">url</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The URL of the storage blob.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="access_tier_python">
<a href="#access_tier_python" style="color: inherit; text-decoration: inherit;">access_<wbr>tier</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The access tier of the storage blob.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="content_md5_python">
<a href="#content_md5_python" style="color: inherit; text-decoration: inherit;">content_<wbr>md5</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The MD5 sum of the blob contents.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="content_type_python">
<a href="#content_type_python" style="color: inherit; text-decoration: inherit;">content_<wbr>type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The content type of the storage blob.
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
        <span id="metadata_python">
<a href="#metadata_python" style="color: inherit; text-decoration: inherit;">metadata</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Mapping[str, str]</span>
    </dt>
    <dd>{{% md %}}A map of custom blob metadata.
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
        <span id="storage_account_name_python">
<a href="#storage_account_name_python" style="color: inherit; text-decoration: inherit;">storage_<wbr>account_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="storage_container_name_python">
<a href="#storage_container_name_python" style="color: inherit; text-decoration: inherit;">storage_<wbr>container_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_python">
<a href="#type_python" style="color: inherit; text-decoration: inherit;">type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The type of the storage blob
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="url_python">
<a href="#url_python" style="color: inherit; text-decoration: inherit;">url</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The URL of the storage blob.
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
