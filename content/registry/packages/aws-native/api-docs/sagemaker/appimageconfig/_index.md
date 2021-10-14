
---
title: "AppImageConfig"
title_tag: "aws-native.sagemaker.AppImageConfig"
meta_desc: "Documentation for the aws-native.sagemaker.AppImageConfig resource with examples, input properties, output properties, lookup functions, and supporting types."
layout: api
no_edit_this_page: true
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Resource Type definition for AWS::SageMaker::AppImageConfig




## Create a AppImageConfig Resource {#create}
{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx">AppImageConfig</span><span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">AppImageConfigArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class=nd>@overload</span>
<span class="k">def </span><span class="nx">AppImageConfig</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
                   <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">,</span>
                   <span class="nx">app_image_config_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                   <span class="nx">kernel_gateway_image_config</span><span class="p">:</span> <span class="nx">Optional[AppImageConfigKernelGatewayImageConfigArgs]</span> = None<span class="p">,</span>
                   <span class="nx">tags</span><span class="p">:</span> <span class="nx">Optional[Sequence[AppImageConfigTagArgs]]</span> = None<span class="p">)</span>
<span class=nd>@overload</span>
<span class="k">def </span><span class="nx">AppImageConfig</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
                   <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">AppImageConfigArgs</a></span><span class="p">,</span>
                   <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span><span class="nx">NewAppImageConfig</span><span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">name</span><span class="p"> </span><span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p"> </span><span class="nx"><a href="#inputs">AppImageConfigArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx">AppImageConfig</span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx">AppImageConfig</span><span class="p">(</span><span class="nx">string</span><span class="p"> </span><span class="nx">name<span class="p">,</span> <span class="nx"><a href="#inputs">AppImageConfigArgs</a></span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span class="property-type"><a href="#inputs">AppImageConfigArgs</a></span>
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
        <span class="property-type"><a href="#inputs">AppImageConfigArgs</a></span>
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
        <span class="property-type"><a href="#inputs">AppImageConfigArgs</a></span>
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
        <span class="property-type"><a href="#inputs">AppImageConfigArgs</a></span>
    </dt>
    <dd>The arguments to resource properties.</dd><dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>
    </dt>
    <dd>Bag of options to control resource&#39;s behavior.</dd></dl>

{{% /choosable %}}

## AppImageConfig Resource Properties {#properties}

To learn more about resource properties and how to use them, see [Inputs and Outputs]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) in the Architecture and Concepts docs.

### Inputs

The AppImageConfig resource accepts the following [input]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) properties:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="appimageconfigname_csharp">
<a href="#appimageconfigname_csharp" style="color: inherit; text-decoration: inherit;">App<wbr>Image<wbr>Config<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Name of the AppImageConfig.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="kernelgatewayimageconfig_csharp">
<a href="#kernelgatewayimageconfig_csharp" style="color: inherit; text-decoration: inherit;">Kernel<wbr>Gateway<wbr>Image<wbr>Config</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#appimageconfigkernelgatewayimageconfig">Pulumi.<wbr>Aws<wbr>Native.<wbr>Sage<wbr>Maker.<wbr>Inputs.<wbr>App<wbr>Image<wbr>Config<wbr>Kernel<wbr>Gateway<wbr>Image<wbr>Config<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}The KernelGatewayImageConfig.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="tags_csharp">
<a href="#tags_csharp" style="color: inherit; text-decoration: inherit;">Tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#appimageconfigtag">List&lt;Pulumi.<wbr>Aws<wbr>Native.<wbr>Sage<wbr>Maker.<wbr>Inputs.<wbr>App<wbr>Image<wbr>Config<wbr>Tag<wbr>Args&gt;</a></span>
    </dt>
    <dd>{{% md %}}A list of tags to apply to the AppImageConfig.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="appimageconfigname_go">
<a href="#appimageconfigname_go" style="color: inherit; text-decoration: inherit;">App<wbr>Image<wbr>Config<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Name of the AppImageConfig.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="kernelgatewayimageconfig_go">
<a href="#kernelgatewayimageconfig_go" style="color: inherit; text-decoration: inherit;">Kernel<wbr>Gateway<wbr>Image<wbr>Config</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#appimageconfigkernelgatewayimageconfig">App<wbr>Image<wbr>Config<wbr>Kernel<wbr>Gateway<wbr>Image<wbr>Config<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}The KernelGatewayImageConfig.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="tags_go">
<a href="#tags_go" style="color: inherit; text-decoration: inherit;">Tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#appimageconfigtag">[]App<wbr>Image<wbr>Config<wbr>Tag<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}A list of tags to apply to the AppImageConfig.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="appimageconfigname_nodejs">
<a href="#appimageconfigname_nodejs" style="color: inherit; text-decoration: inherit;">app<wbr>Image<wbr>Config<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Name of the AppImageConfig.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="kernelgatewayimageconfig_nodejs">
<a href="#kernelgatewayimageconfig_nodejs" style="color: inherit; text-decoration: inherit;">kernel<wbr>Gateway<wbr>Image<wbr>Config</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#appimageconfigkernelgatewayimageconfig">App<wbr>Image<wbr>Config<wbr>Kernel<wbr>Gateway<wbr>Image<wbr>Config<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}The KernelGatewayImageConfig.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="tags_nodejs">
<a href="#tags_nodejs" style="color: inherit; text-decoration: inherit;">tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#appimageconfigtag">App<wbr>Image<wbr>Config<wbr>Tag<wbr>Args[]</a></span>
    </dt>
    <dd>{{% md %}}A list of tags to apply to the AppImageConfig.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="app_image_config_name_python">
<a href="#app_image_config_name_python" style="color: inherit; text-decoration: inherit;">app_<wbr>image_<wbr>config_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The Name of the AppImageConfig.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="kernel_gateway_image_config_python">
<a href="#kernel_gateway_image_config_python" style="color: inherit; text-decoration: inherit;">kernel_<wbr>gateway_<wbr>image_<wbr>config</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#appimageconfigkernelgatewayimageconfig">App<wbr>Image<wbr>Config<wbr>Kernel<wbr>Gateway<wbr>Image<wbr>Config<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}The KernelGatewayImageConfig.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="tags_python">
<a href="#tags_python" style="color: inherit; text-decoration: inherit;">tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#appimageconfigtag">Sequence[App<wbr>Image<wbr>Config<wbr>Tag<wbr>Args]</a></span>
    </dt>
    <dd>{{% md %}}A list of tags to apply to the AppImageConfig.{{% /md %}}</dd></dl>
{{% /choosable %}}


### Outputs

All [input](#inputs) properties are implicitly available as output properties. Additionally, the AppImageConfig resource produces the following output properties:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="appimageconfigarn_csharp">
<a href="#appimageconfigarn_csharp" style="color: inherit; text-decoration: inherit;">App<wbr>Image<wbr>Config<wbr>Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) of the AppImageConfig.{{% /md %}}</dd><dt class="property-"
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
        <span id="appimageconfigarn_go">
<a href="#appimageconfigarn_go" style="color: inherit; text-decoration: inherit;">App<wbr>Image<wbr>Config<wbr>Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) of the AppImageConfig.{{% /md %}}</dd><dt class="property-"
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
        <span id="appimageconfigarn_nodejs">
<a href="#appimageconfigarn_nodejs" style="color: inherit; text-decoration: inherit;">app<wbr>Image<wbr>Config<wbr>Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) of the AppImageConfig.{{% /md %}}</dd><dt class="property-"
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
        <span id="app_image_config_arn_python">
<a href="#app_image_config_arn_python" style="color: inherit; text-decoration: inherit;">app_<wbr>image_<wbr>config_<wbr>arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) of the AppImageConfig.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_python">
<a href="#id_python" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd></dl>
{{% /choosable %}}







## Supporting Types



<h4 id="appimageconfigfilesystemconfig">App<wbr>Image<wbr>Config<wbr>File<wbr>System<wbr>Config</h4>

{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="defaultgid_csharp">
<a href="#defaultgid_csharp" style="color: inherit; text-decoration: inherit;">Default<wbr>Gid</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The default POSIX group ID (GID). If not specified, defaults to 100.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="defaultuid_csharp">
<a href="#defaultuid_csharp" style="color: inherit; text-decoration: inherit;">Default<wbr>Uid</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The default POSIX user ID (UID). If not specified, defaults to 1000.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="mountpath_csharp">
<a href="#mountpath_csharp" style="color: inherit; text-decoration: inherit;">Mount<wbr>Path</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The path within the image to mount the user's EFS home directory. The directory should be empty. If not specified, defaults to /home/sagemaker-user.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="defaultgid_go">
<a href="#defaultgid_go" style="color: inherit; text-decoration: inherit;">Default<wbr>Gid</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The default POSIX group ID (GID). If not specified, defaults to 100.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="defaultuid_go">
<a href="#defaultuid_go" style="color: inherit; text-decoration: inherit;">Default<wbr>Uid</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The default POSIX user ID (UID). If not specified, defaults to 1000.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="mountpath_go">
<a href="#mountpath_go" style="color: inherit; text-decoration: inherit;">Mount<wbr>Path</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The path within the image to mount the user's EFS home directory. The directory should be empty. If not specified, defaults to /home/sagemaker-user.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="defaultgid_nodejs">
<a href="#defaultgid_nodejs" style="color: inherit; text-decoration: inherit;">default<wbr>Gid</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The default POSIX group ID (GID). If not specified, defaults to 100.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="defaultuid_nodejs">
<a href="#defaultuid_nodejs" style="color: inherit; text-decoration: inherit;">default<wbr>Uid</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The default POSIX user ID (UID). If not specified, defaults to 1000.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="mountpath_nodejs">
<a href="#mountpath_nodejs" style="color: inherit; text-decoration: inherit;">mount<wbr>Path</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The path within the image to mount the user's EFS home directory. The directory should be empty. If not specified, defaults to /home/sagemaker-user.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="default_gid_python">
<a href="#default_gid_python" style="color: inherit; text-decoration: inherit;">default_<wbr>gid</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The default POSIX group ID (GID). If not specified, defaults to 100.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="default_uid_python">
<a href="#default_uid_python" style="color: inherit; text-decoration: inherit;">default_<wbr>uid</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The default POSIX user ID (UID). If not specified, defaults to 1000.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="mount_path_python">
<a href="#mount_path_python" style="color: inherit; text-decoration: inherit;">mount_<wbr>path</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The path within the image to mount the user's EFS home directory. The directory should be empty. If not specified, defaults to /home/sagemaker-user.{{% /md %}}</dd></dl>
{{% /choosable %}}

<h4 id="appimageconfigkernelgatewayimageconfig">App<wbr>Image<wbr>Config<wbr>Kernel<wbr>Gateway<wbr>Image<wbr>Config</h4>

{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="kernelspecs_csharp">
<a href="#kernelspecs_csharp" style="color: inherit; text-decoration: inherit;">Kernel<wbr>Specs</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#appimageconfigkernelspec">List&lt;Pulumi.<wbr>Aws<wbr>Native.<wbr>Sage<wbr>Maker.<wbr>Inputs.<wbr>App<wbr>Image<wbr>Config<wbr>Kernel<wbr>Spec&gt;</a></span>
    </dt>
    <dd>{{% md %}}The specification of the Jupyter kernels in the image.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="filesystemconfig_csharp">
<a href="#filesystemconfig_csharp" style="color: inherit; text-decoration: inherit;">File<wbr>System<wbr>Config</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#appimageconfigfilesystemconfig">Pulumi.<wbr>Aws<wbr>Native.<wbr>Sage<wbr>Maker.<wbr>Inputs.<wbr>App<wbr>Image<wbr>Config<wbr>File<wbr>System<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}The Amazon Elastic File System (EFS) storage configuration for a SageMaker image.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="kernelspecs_go">
<a href="#kernelspecs_go" style="color: inherit; text-decoration: inherit;">Kernel<wbr>Specs</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#appimageconfigkernelspec">[]App<wbr>Image<wbr>Config<wbr>Kernel<wbr>Spec</a></span>
    </dt>
    <dd>{{% md %}}The specification of the Jupyter kernels in the image.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="filesystemconfig_go">
<a href="#filesystemconfig_go" style="color: inherit; text-decoration: inherit;">File<wbr>System<wbr>Config</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#appimageconfigfilesystemconfig">App<wbr>Image<wbr>Config<wbr>File<wbr>System<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}The Amazon Elastic File System (EFS) storage configuration for a SageMaker image.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="kernelspecs_nodejs">
<a href="#kernelspecs_nodejs" style="color: inherit; text-decoration: inherit;">kernel<wbr>Specs</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#appimageconfigkernelspec">App<wbr>Image<wbr>Config<wbr>Kernel<wbr>Spec[]</a></span>
    </dt>
    <dd>{{% md %}}The specification of the Jupyter kernels in the image.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="filesystemconfig_nodejs">
<a href="#filesystemconfig_nodejs" style="color: inherit; text-decoration: inherit;">file<wbr>System<wbr>Config</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#appimageconfigfilesystemconfig">App<wbr>Image<wbr>Config<wbr>File<wbr>System<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}The Amazon Elastic File System (EFS) storage configuration for a SageMaker image.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="kernel_specs_python">
<a href="#kernel_specs_python" style="color: inherit; text-decoration: inherit;">kernel_<wbr>specs</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#appimageconfigkernelspec">Sequence[App<wbr>Image<wbr>Config<wbr>Kernel<wbr>Spec]</a></span>
    </dt>
    <dd>{{% md %}}The specification of the Jupyter kernels in the image.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="file_system_config_python">
<a href="#file_system_config_python" style="color: inherit; text-decoration: inherit;">file_<wbr>system_<wbr>config</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#appimageconfigfilesystemconfig">App<wbr>Image<wbr>Config<wbr>File<wbr>System<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}The Amazon Elastic File System (EFS) storage configuration for a SageMaker image.{{% /md %}}</dd></dl>
{{% /choosable %}}

<h4 id="appimageconfigkernelspec">App<wbr>Image<wbr>Config<wbr>Kernel<wbr>Spec</h4>

{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the kernel.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="displayname_csharp">
<a href="#displayname_csharp" style="color: inherit; text-decoration: inherit;">Display<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The display name of the kernel.{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}The name of the kernel.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="displayname_go">
<a href="#displayname_go" style="color: inherit; text-decoration: inherit;">Display<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The display name of the kernel.{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}The name of the kernel.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="displayname_nodejs">
<a href="#displayname_nodejs" style="color: inherit; text-decoration: inherit;">display<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The display name of the kernel.{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}The name of the kernel.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="display_name_python">
<a href="#display_name_python" style="color: inherit; text-decoration: inherit;">display_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The display name of the kernel.{{% /md %}}</dd></dl>
{{% /choosable %}}

<h4 id="appimageconfigtag">App<wbr>Image<wbr>Config<wbr>Tag</h4>

{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="key_csharp">
<a href="#key_csharp" style="color: inherit; text-decoration: inherit;">Key</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="value_csharp">
<a href="#value_csharp" style="color: inherit; text-decoration: inherit;">Value</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="key_go">
<a href="#key_go" style="color: inherit; text-decoration: inherit;">Key</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="value_go">
<a href="#value_go" style="color: inherit; text-decoration: inherit;">Value</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="key_nodejs">
<a href="#key_nodejs" style="color: inherit; text-decoration: inherit;">key</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="value_nodejs">
<a href="#value_nodejs" style="color: inherit; text-decoration: inherit;">value</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="key_python">
<a href="#key_python" style="color: inherit; text-decoration: inherit;">key</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="value_python">
<a href="#value_python" style="color: inherit; text-decoration: inherit;">value</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}


<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-aws-native">https://github.com/pulumi/pulumi-aws-native</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
</dl>
