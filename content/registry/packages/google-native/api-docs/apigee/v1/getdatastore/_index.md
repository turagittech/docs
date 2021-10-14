
---
title: "getDatastore"
title_tag: "google-native.apigee/v1.getDatastore"
meta_desc: "Documentation for the google-native.apigee/v1.getDatastore function with examples, input properties, output properties, and supporting types."
layout: api
no_edit_this_page: true
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Get a Datastore




## Using getDatastore {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getDatastore<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetDatastoreArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetDatastoreResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>get_datastore(</span><span class="nx">datastore_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                  <span class="nx">organization_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                  <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> GetDatastoreResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>LookupDatastore<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">args</span><span class="p"> *</span><span class="nx">LookupDatastoreArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">LookupDatastoreResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `LookupDatastore` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetDatastore </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetDatastoreResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">GetDatastoreArgs</span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="datastoreid_csharp">
<a href="#datastoreid_csharp" style="color: inherit; text-decoration: inherit;">Datastore<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="organizationid_csharp">
<a href="#organizationid_csharp" style="color: inherit; text-decoration: inherit;">Organization<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="datastoreid_go">
<a href="#datastoreid_go" style="color: inherit; text-decoration: inherit;">Datastore<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="organizationid_go">
<a href="#organizationid_go" style="color: inherit; text-decoration: inherit;">Organization<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="datastoreid_nodejs">
<a href="#datastoreid_nodejs" style="color: inherit; text-decoration: inherit;">datastore<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="organizationid_nodejs">
<a href="#organizationid_nodejs" style="color: inherit; text-decoration: inherit;">organization<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="datastore_id_python">
<a href="#datastore_id_python" style="color: inherit; text-decoration: inherit;">datastore_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="organization_id_python">
<a href="#organization_id_python" style="color: inherit; text-decoration: inherit;">organization_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}




## getDatastore Result {#result}

The following output properties are available:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="createtime_csharp">
<a href="#createtime_csharp" style="color: inherit; text-decoration: inherit;">Create<wbr>Time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Datastore create time, in milliseconds since the epoch of 1970-01-01T00:00:00Z{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="datastoreconfig_csharp">
<a href="#datastoreconfig_csharp" style="color: inherit; text-decoration: inherit;">Datastore<wbr>Config</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#googlecloudapigeev1datastoreconfigresponse">Pulumi.<wbr>Google<wbr>Native.<wbr>Apigee.<wbr>V1.<wbr>Outputs.<wbr>Google<wbr>Cloud<wbr>Apigee<wbr>V1Datastore<wbr>Config<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Datastore Configurations.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="displayname_csharp">
<a href="#displayname_csharp" style="color: inherit; text-decoration: inherit;">Display<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Display name in UI{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="lastupdatetime_csharp">
<a href="#lastupdatetime_csharp" style="color: inherit; text-decoration: inherit;">Last<wbr>Update<wbr>Time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Datastore last update time, in milliseconds since the epoch of 1970-01-01T00:00:00Z{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="org_csharp">
<a href="#org_csharp" style="color: inherit; text-decoration: inherit;">Org</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Organization that the datastore belongs to{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="self_csharp">
<a href="#self_csharp" style="color: inherit; text-decoration: inherit;">Self</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource link of Datastore. Example: `/organizations/{org}/analytics/datastores/{uuid}`{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="targettype_csharp">
<a href="#targettype_csharp" style="color: inherit; text-decoration: inherit;">Target<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Destination storage type. Supported types `gcs` or `bigquery`.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="createtime_go">
<a href="#createtime_go" style="color: inherit; text-decoration: inherit;">Create<wbr>Time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Datastore create time, in milliseconds since the epoch of 1970-01-01T00:00:00Z{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="datastoreconfig_go">
<a href="#datastoreconfig_go" style="color: inherit; text-decoration: inherit;">Datastore<wbr>Config</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#googlecloudapigeev1datastoreconfigresponse">Google<wbr>Cloud<wbr>Apigee<wbr>V1Datastore<wbr>Config<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Datastore Configurations.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="displayname_go">
<a href="#displayname_go" style="color: inherit; text-decoration: inherit;">Display<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Display name in UI{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="lastupdatetime_go">
<a href="#lastupdatetime_go" style="color: inherit; text-decoration: inherit;">Last<wbr>Update<wbr>Time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Datastore last update time, in milliseconds since the epoch of 1970-01-01T00:00:00Z{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="org_go">
<a href="#org_go" style="color: inherit; text-decoration: inherit;">Org</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Organization that the datastore belongs to{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="self_go">
<a href="#self_go" style="color: inherit; text-decoration: inherit;">Self</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource link of Datastore. Example: `/organizations/{org}/analytics/datastores/{uuid}`{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="targettype_go">
<a href="#targettype_go" style="color: inherit; text-decoration: inherit;">Target<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Destination storage type. Supported types `gcs` or `bigquery`.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="createtime_nodejs">
<a href="#createtime_nodejs" style="color: inherit; text-decoration: inherit;">create<wbr>Time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Datastore create time, in milliseconds since the epoch of 1970-01-01T00:00:00Z{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="datastoreconfig_nodejs">
<a href="#datastoreconfig_nodejs" style="color: inherit; text-decoration: inherit;">datastore<wbr>Config</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#googlecloudapigeev1datastoreconfigresponse">Google<wbr>Cloud<wbr>Apigee<wbr>V1Datastore<wbr>Config<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Datastore Configurations.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="displayname_nodejs">
<a href="#displayname_nodejs" style="color: inherit; text-decoration: inherit;">display<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Display name in UI{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="lastupdatetime_nodejs">
<a href="#lastupdatetime_nodejs" style="color: inherit; text-decoration: inherit;">last<wbr>Update<wbr>Time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Datastore last update time, in milliseconds since the epoch of 1970-01-01T00:00:00Z{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="org_nodejs">
<a href="#org_nodejs" style="color: inherit; text-decoration: inherit;">org</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Organization that the datastore belongs to{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="self_nodejs">
<a href="#self_nodejs" style="color: inherit; text-decoration: inherit;">self</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource link of Datastore. Example: `/organizations/{org}/analytics/datastores/{uuid}`{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="targettype_nodejs">
<a href="#targettype_nodejs" style="color: inherit; text-decoration: inherit;">target<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Destination storage type. Supported types `gcs` or `bigquery`.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="create_time_python">
<a href="#create_time_python" style="color: inherit; text-decoration: inherit;">create_<wbr>time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Datastore create time, in milliseconds since the epoch of 1970-01-01T00:00:00Z{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="datastore_config_python">
<a href="#datastore_config_python" style="color: inherit; text-decoration: inherit;">datastore_<wbr>config</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#googlecloudapigeev1datastoreconfigresponse">Google<wbr>Cloud<wbr>Apigee<wbr>V1Datastore<wbr>Config<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Datastore Configurations.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="display_name_python">
<a href="#display_name_python" style="color: inherit; text-decoration: inherit;">display_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Display name in UI{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="last_update_time_python">
<a href="#last_update_time_python" style="color: inherit; text-decoration: inherit;">last_<wbr>update_<wbr>time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Datastore last update time, in milliseconds since the epoch of 1970-01-01T00:00:00Z{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="org_python">
<a href="#org_python" style="color: inherit; text-decoration: inherit;">org</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Organization that the datastore belongs to{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="self_python">
<a href="#self_python" style="color: inherit; text-decoration: inherit;">self</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Resource link of Datastore. Example: `/organizations/{org}/analytics/datastores/{uuid}`{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="target_type_python">
<a href="#target_type_python" style="color: inherit; text-decoration: inherit;">target_<wbr>type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Destination storage type. Supported types `gcs` or `bigquery`.{{% /md %}}</dd></dl>
{{% /choosable %}}




## Supporting Types


<h4 id="googlecloudapigeev1datastoreconfigresponse">Google<wbr>Cloud<wbr>Apigee<wbr>V1Datastore<wbr>Config<wbr>Response</h4>



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="bucketname_csharp">
<a href="#bucketname_csharp" style="color: inherit; text-decoration: inherit;">Bucket<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of the Cloud Storage bucket. Required for `gcs` target_type.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="datasetname_csharp">
<a href="#datasetname_csharp" style="color: inherit; text-decoration: inherit;">Dataset<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}BigQuery dataset name Required for `bigquery` target_type.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="path_csharp">
<a href="#path_csharp" style="color: inherit; text-decoration: inherit;">Path</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Path of Cloud Storage bucket Required for `gcs` target_type.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="project_csharp">
<a href="#project_csharp" style="color: inherit; text-decoration: inherit;">Project</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}GCP project in which the datastore exists{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="tableprefix_csharp">
<a href="#tableprefix_csharp" style="color: inherit; text-decoration: inherit;">Table<wbr>Prefix</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Prefix of BigQuery table Required for `bigquery` target_type.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="bucketname_go">
<a href="#bucketname_go" style="color: inherit; text-decoration: inherit;">Bucket<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of the Cloud Storage bucket. Required for `gcs` target_type.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="datasetname_go">
<a href="#datasetname_go" style="color: inherit; text-decoration: inherit;">Dataset<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}BigQuery dataset name Required for `bigquery` target_type.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="path_go">
<a href="#path_go" style="color: inherit; text-decoration: inherit;">Path</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Path of Cloud Storage bucket Required for `gcs` target_type.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="project_go">
<a href="#project_go" style="color: inherit; text-decoration: inherit;">Project</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}GCP project in which the datastore exists{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="tableprefix_go">
<a href="#tableprefix_go" style="color: inherit; text-decoration: inherit;">Table<wbr>Prefix</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Prefix of BigQuery table Required for `bigquery` target_type.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="bucketname_nodejs">
<a href="#bucketname_nodejs" style="color: inherit; text-decoration: inherit;">bucket<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of the Cloud Storage bucket. Required for `gcs` target_type.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="datasetname_nodejs">
<a href="#datasetname_nodejs" style="color: inherit; text-decoration: inherit;">dataset<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}BigQuery dataset name Required for `bigquery` target_type.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="path_nodejs">
<a href="#path_nodejs" style="color: inherit; text-decoration: inherit;">path</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Path of Cloud Storage bucket Required for `gcs` target_type.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="project_nodejs">
<a href="#project_nodejs" style="color: inherit; text-decoration: inherit;">project</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}GCP project in which the datastore exists{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="tableprefix_nodejs">
<a href="#tableprefix_nodejs" style="color: inherit; text-decoration: inherit;">table<wbr>Prefix</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Prefix of BigQuery table Required for `bigquery` target_type.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="bucket_name_python">
<a href="#bucket_name_python" style="color: inherit; text-decoration: inherit;">bucket_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Name of the Cloud Storage bucket. Required for `gcs` target_type.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="dataset_name_python">
<a href="#dataset_name_python" style="color: inherit; text-decoration: inherit;">dataset_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}BigQuery dataset name Required for `bigquery` target_type.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="path_python">
<a href="#path_python" style="color: inherit; text-decoration: inherit;">path</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Path of Cloud Storage bucket Required for `gcs` target_type.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="project_python">
<a href="#project_python" style="color: inherit; text-decoration: inherit;">project</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}GCP project in which the datastore exists{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="table_prefix_python">
<a href="#table_prefix_python" style="color: inherit; text-decoration: inherit;">table_<wbr>prefix</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Prefix of BigQuery table Required for `bigquery` target_type.{{% /md %}}</dd></dl>
{{% /choosable %}}





<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-google-native">https://github.com/pulumi/pulumi-google-native</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
</dl>
