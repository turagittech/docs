
---
title: "getDebugSession"
title_tag: "google-native.apigee/v1.getDebugSession"
meta_desc: "Documentation for the google-native.apigee/v1.getDebugSession function with examples, input properties, output properties, and supporting types."
layout: api
no_edit_this_page: true
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Retrieves a debug session.




## Using getDebugSession {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getDebugSession<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetDebugSessionArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetDebugSessionResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>get_debug_session(</span><span class="nx">api_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                      <span class="nx">debugsession_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                      <span class="nx">environment_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                      <span class="nx">organization_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                      <span class="nx">revision_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                      <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> GetDebugSessionResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>LookupDebugSession<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">args</span><span class="p"> *</span><span class="nx">LookupDebugSessionArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">LookupDebugSessionResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `LookupDebugSession` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetDebugSession </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetDebugSessionResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">GetDebugSessionArgs</span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="apiid_csharp">
<a href="#apiid_csharp" style="color: inherit; text-decoration: inherit;">Api<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="debugsessionid_csharp">
<a href="#debugsessionid_csharp" style="color: inherit; text-decoration: inherit;">Debugsession<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="environmentid_csharp">
<a href="#environmentid_csharp" style="color: inherit; text-decoration: inherit;">Environment<wbr>Id</a>
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
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="revisionid_csharp">
<a href="#revisionid_csharp" style="color: inherit; text-decoration: inherit;">Revision<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="apiid_go">
<a href="#apiid_go" style="color: inherit; text-decoration: inherit;">Api<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="debugsessionid_go">
<a href="#debugsessionid_go" style="color: inherit; text-decoration: inherit;">Debugsession<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="environmentid_go">
<a href="#environmentid_go" style="color: inherit; text-decoration: inherit;">Environment<wbr>Id</a>
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
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="revisionid_go">
<a href="#revisionid_go" style="color: inherit; text-decoration: inherit;">Revision<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="apiid_nodejs">
<a href="#apiid_nodejs" style="color: inherit; text-decoration: inherit;">api<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="debugsessionid_nodejs">
<a href="#debugsessionid_nodejs" style="color: inherit; text-decoration: inherit;">debugsession<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="environmentid_nodejs">
<a href="#environmentid_nodejs" style="color: inherit; text-decoration: inherit;">environment<wbr>Id</a>
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
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="revisionid_nodejs">
<a href="#revisionid_nodejs" style="color: inherit; text-decoration: inherit;">revision<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="api_id_python">
<a href="#api_id_python" style="color: inherit; text-decoration: inherit;">api_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="debugsession_id_python">
<a href="#debugsession_id_python" style="color: inherit; text-decoration: inherit;">debugsession_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="environment_id_python">
<a href="#environment_id_python" style="color: inherit; text-decoration: inherit;">environment_<wbr>id</a>
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
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="revision_id_python">
<a href="#revision_id_python" style="color: inherit; text-decoration: inherit;">revision_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}




## getDebugSession Result {#result}

The following output properties are available:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="count_csharp">
<a href="#count_csharp" style="color: inherit; text-decoration: inherit;">Count</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Optional. The number of request to be traced. Min = 1, Max = 15, Default = 10.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="filter_csharp">
<a href="#filter_csharp" style="color: inherit; text-decoration: inherit;">Filter</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Optional. A conditional statement which is evaluated against the request message to determine if it should be traced. Syntax matches that of on API Proxy bundle flow Condition.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A unique ID for this DebugSession.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="timeout_csharp">
<a href="#timeout_csharp" style="color: inherit; text-decoration: inherit;">Timeout</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Optional. The time in seconds after which this DebugSession should end. This value will override the value in query param, if both are provided.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="tracesize_csharp">
<a href="#tracesize_csharp" style="color: inherit; text-decoration: inherit;">Tracesize</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Optional. The maximum number of bytes captured from the response payload. Min = 0, Max = 5120, Default = 5120.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="validity_csharp">
<a href="#validity_csharp" style="color: inherit; text-decoration: inherit;">Validity</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Optional. The length of time, in seconds, that this debug session is valid, starting from when it's received in the control plane. Min = 1, Max = 15, Default = 10.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="count_go">
<a href="#count_go" style="color: inherit; text-decoration: inherit;">Count</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Optional. The number of request to be traced. Min = 1, Max = 15, Default = 10.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="filter_go">
<a href="#filter_go" style="color: inherit; text-decoration: inherit;">Filter</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Optional. A conditional statement which is evaluated against the request message to determine if it should be traced. Syntax matches that of on API Proxy bundle flow Condition.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_go">
<a href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A unique ID for this DebugSession.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="timeout_go">
<a href="#timeout_go" style="color: inherit; text-decoration: inherit;">Timeout</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Optional. The time in seconds after which this DebugSession should end. This value will override the value in query param, if both are provided.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="tracesize_go">
<a href="#tracesize_go" style="color: inherit; text-decoration: inherit;">Tracesize</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Optional. The maximum number of bytes captured from the response payload. Min = 0, Max = 5120, Default = 5120.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="validity_go">
<a href="#validity_go" style="color: inherit; text-decoration: inherit;">Validity</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Optional. The length of time, in seconds, that this debug session is valid, starting from when it's received in the control plane. Min = 1, Max = 15, Default = 10.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="count_nodejs">
<a href="#count_nodejs" style="color: inherit; text-decoration: inherit;">count</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}Optional. The number of request to be traced. Min = 1, Max = 15, Default = 10.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="filter_nodejs">
<a href="#filter_nodejs" style="color: inherit; text-decoration: inherit;">filter</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Optional. A conditional statement which is evaluated against the request message to determine if it should be traced. Syntax matches that of on API Proxy bundle flow Condition.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_nodejs">
<a href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A unique ID for this DebugSession.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="timeout_nodejs">
<a href="#timeout_nodejs" style="color: inherit; text-decoration: inherit;">timeout</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Optional. The time in seconds after which this DebugSession should end. This value will override the value in query param, if both are provided.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="tracesize_nodejs">
<a href="#tracesize_nodejs" style="color: inherit; text-decoration: inherit;">tracesize</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}Optional. The maximum number of bytes captured from the response payload. Min = 0, Max = 5120, Default = 5120.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="validity_nodejs">
<a href="#validity_nodejs" style="color: inherit; text-decoration: inherit;">validity</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}Optional. The length of time, in seconds, that this debug session is valid, starting from when it's received in the control plane. Min = 1, Max = 15, Default = 10.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="count_python">
<a href="#count_python" style="color: inherit; text-decoration: inherit;">count</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Optional. The number of request to be traced. Min = 1, Max = 15, Default = 10.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="filter_python">
<a href="#filter_python" style="color: inherit; text-decoration: inherit;">filter</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Optional. A conditional statement which is evaluated against the request message to determine if it should be traced. Syntax matches that of on API Proxy bundle flow Condition.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_python">
<a href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A unique ID for this DebugSession.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="timeout_python">
<a href="#timeout_python" style="color: inherit; text-decoration: inherit;">timeout</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Optional. The time in seconds after which this DebugSession should end. This value will override the value in query param, if both are provided.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="tracesize_python">
<a href="#tracesize_python" style="color: inherit; text-decoration: inherit;">tracesize</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Optional. The maximum number of bytes captured from the response payload. Min = 0, Max = 5120, Default = 5120.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="validity_python">
<a href="#validity_python" style="color: inherit; text-decoration: inherit;">validity</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Optional. The length of time, in seconds, that this debug session is valid, starting from when it's received in the control plane. Min = 1, Max = 15, Default = 10.{{% /md %}}</dd></dl>
{{% /choosable %}}





<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-google-native">https://github.com/pulumi/pulumi-google-native</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
</dl>
