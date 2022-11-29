---
title: "Module classic/cloudfront"
title_tag: "Module classic/cloudfront | Package @pulumi/awsx | Node.js SDK"
linktitle: "cloudfront"
meta_desc: "Explore members of the cloudfront module in the @pulumi/awsx package."
git_sha: "43b8dabc0ec1e5187bf63e107bf06ee54021a1a7"
---

<!-- WARNING: this page was generated by a tool. Do not edit it by hand. -->
<!-- To change it, please see https://github.com/pulumi/docs/tree/master/tools/tscdocgen. -->

{{< resource-docs-alert "awsx" >}}






<h3>APIs</h3>
<ul class="api">
    <li><a href="#metrics"><span class="symbol api"></span>metrics</a></li>
</ul>




<h2 id="apis">APIs</h2>
<h3 class="pdoc-module-header" id="metrics" data-link-title="metrics">
    <a href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/cloudfront/metrics.ts#L20">
        namespace <strong>metrics</strong>
    </a>
</h3>

<h4 class="pdoc-member-header" id="bytesDownloaded">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/cloudfront/metrics.ts#L87">function <b>bytesDownloaded</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span>bytesDownloaded(change?: <a href='#CloudfrontMetricChange'>CloudfrontMetricChange</a>): <a href='/docs/reference/pkg/nodejs/pulumi/awsx/classic/cloudwatch/#Metric'>Metric</a></code></pre>


The number of bytes downloaded by viewers for GET, HEAD, and OPTIONS requests.

Valid Statistics: Sum
Units: None

<h4 class="pdoc-member-header" id="bytesUploaded">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/cloudfront/metrics.ts#L97">function <b>bytesUploaded</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span>bytesUploaded(change?: <a href='#CloudfrontMetricChange'>CloudfrontMetricChange</a>): <a href='/docs/reference/pkg/nodejs/pulumi/awsx/classic/cloudwatch/#Metric'>Metric</a></code></pre>


The number of bytes uploaded to your origin with CloudFront using POST and PUT requests.

Valid Statistics: Sum
Units: None

<h4 class="pdoc-member-header" id="CloudfrontMetricChange">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/cloudfront/metrics.ts#L25">interface <b>CloudfrontMetricChange</b></a>
</h4>

<pre class="highlight"><code><span class='kr'>interface</span> <span class='nx'>CloudfrontMetricChange</span> <span class='kr'>extends</span> <a href='/docs/reference/pkg/nodejs/pulumi/awsx/classic/cloudwatch/#MetricChange'>MetricChange</a></code></pre>
<h4 class="pdoc-member-header" id="CloudfrontMetricChange-color">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/cloudwatch/metric.ts#L464">property <b>color</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>color?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

The six-digit HTML hex color code to be used for this metric.

Only used if this metric is displayed in a [Dashboard] with a [MetricWidget].

<h4 class="pdoc-member-header" id="CloudfrontMetricChange-dimensions">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/cloudwatch/metric.ts#L433">property <b>dimensions</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>dimensions?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;Record&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;&gt;&gt;;</code></pre>

The new dimension for this metric.  If this object is missing this property, then no change
will be made.  However, if the property is there by set to [undefined] then the value will be
cleared.

<h4 class="pdoc-member-header" id="CloudfrontMetricChange-distribution">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/cloudfront/metrics.ts#L29">property <b>distribution</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>distribution?: <a href='/docs/reference/pkg/nodejs/pulumi/aws/cloudfront/#Distribution'>aws.cloudfront.Distribution</a>;</code></pre>

Optional [Distribution] this metric should be filtered down to.

<h4 class="pdoc-member-header" id="CloudfrontMetricChange-extendedStatistic">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/cloudwatch/metric.ts#L451">property <b>extendedStatistic</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>extendedStatistic?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number'>number</a></span>&gt;;</code></pre>

The new percentile statistic for the metric associated with the alarm.  If this object is
missing this property, then no change will be made.  However, if the property is there by set
to [undefined] then the value will be set to the default.

<h4 class="pdoc-member-header" id="CloudfrontMetricChange-label">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/cloudwatch/metric.ts#L473">property <b>label</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>label?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

The label to display for this metric in the graph legend. If this is not specified, the
metric is given an autogenerated label that distinguishes it from the other metrics in the
widget.

Only used if this metric is displayed in a [Dashboard] with a [MetricWidget].

<h4 class="pdoc-member-header" id="CloudfrontMetricChange-period">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/cloudwatch/metric.ts#L439">property <b>period</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>period?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number'>number</a></span>&gt;;</code></pre>

The new period in seconds over which the specified `stat` is applied.  If this object is
missing this property, then no change will be made.  However, if the property is there by set
to [undefined] then the value will be set to the default (300s).

<h4 class="pdoc-member-header" id="CloudfrontMetricChange-region">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/cloudfront/metrics.ts#L36">property <b>region</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>region?: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</code></pre>

The region for which you want to display metrics. This value must be Global. The Region
dimension is different from the region in which CloudFront metrics are stored, which is
US East (N. Virginia).

<h4 class="pdoc-member-header" id="CloudfrontMetricChange-statistic">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/cloudwatch/metric.ts#L445">property <b>statistic</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>statistic?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/awsx/classic/cloudwatch/#MetricStatistic'>MetricStatistic</a>&gt;;</code></pre>

The new statistic to apply to the alarm's associated metric.  If this object is missing this
property, then no change will be made.  However, if the property is there by set to
[undefined] then the value will be set to the default.

<h4 class="pdoc-member-header" id="CloudfrontMetricChange-unit">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/cloudwatch/metric.ts#L457">property <b>unit</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>unit?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/awsx/classic/cloudwatch/#MetricUnit'>MetricUnit</a>&gt;;</code></pre>

The new unit for this metric.   If this object is missing this property, then no change will
be made.  However, if the property is there by set to [undefined] then the value will be set
to the default.

<h4 class="pdoc-member-header" id="CloudfrontMetricChange-visible">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/cloudwatch/metric.ts#L481">property <b>visible</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>visible?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean'>boolean</a></span>&gt;;</code></pre>

Set this to true to have the metric appear in the graph, or false to have it be hidden. The
default is true.

Only used if this metric is displayed in a [Dashboard] with a [MetricWidget].

<h4 class="pdoc-member-header" id="CloudfrontMetricChange-yAxis">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/cloudwatch/metric.ts#L488">property <b>yAxis</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>yAxis?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='s2'>"left"</span> | <span class='s2'>"right"</span>&gt;;</code></pre>

Where on the graph to display the y-axis for this metric. The default is left.

Only used if this metric is displayed in a [Dashboard] with a [MetricWidget].

<h4 class="pdoc-member-header" id="CloudfrontMetricName">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/cloudfront/metrics.ts#L21">type <b>CloudfrontMetricName</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>type</span> CloudfrontMetricName = <span class='s2'>"Requests"</span> | <span class='s2'>"BytesDownloaded"</span> | <span class='s2'>"BytesUploaded"</span> | <span class='s2'>"TotalErrorRate"</span> | <span class='s2'>"4xxErrorRate"</span> | <span class='s2'>"5xxErrorRate"</span>;</code></pre>
<h4 class="pdoc-member-header" id="errorRate4xx">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/cloudfront/metrics.ts#L117">function <b>errorRate4xx</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span>errorRate4xx(change?: <a href='#CloudfrontMetricChange'>CloudfrontMetricChange</a>): <a href='/docs/reference/pkg/nodejs/pulumi/awsx/classic/cloudwatch/#Metric'>Metric</a></code></pre>


The percentage of all requests for which the HTTP status code is 4xx.

Valid Statistics: Average
Units: Percent

<h4 class="pdoc-member-header" id="errorRate5xx">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/cloudfront/metrics.ts#L127">function <b>errorRate5xx</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span>errorRate5xx(change?: <a href='#CloudfrontMetricChange'>CloudfrontMetricChange</a>): <a href='/docs/reference/pkg/nodejs/pulumi/awsx/classic/cloudwatch/#Metric'>Metric</a></code></pre>


The percentage of all requests for which the HTTP status code is 5xx.

Valid Statistics: Average
Units: Percent

<h4 class="pdoc-member-header" id="metric">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/cloudfront/metrics.ts#L54">function <b>metric</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span>metric(metricName: <a href='#CloudfrontMetricName'>CloudfrontMetricName</a>, change: <a href='#CloudfrontMetricChange'>CloudfrontMetricChange</a>): <a href='/docs/reference/pkg/nodejs/pulumi/awsx/classic/cloudwatch/#Metric'>Metric</a></code></pre>


Creates an AWS/CloudFront metric with the requested [metricName]. See
https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/monitoring-using-cloudwatch.html
for list of all metric-names.

Note, individual metrics can easily be obtained without supplying the name using the other
[metricXXX] functions.

CloudFront metrics use the CloudFront namespace and provide metrics for two dimensions:

1. "DistributionId": The CloudFront ID of the distribution for which you want to display metrics.
2. "Region": The region for which you want to display metrics. This value must be Global. The
   Region dimension is different from the region in which CloudFront metrics are stored, which is
   US East (N. Virginia).

<h4 class="pdoc-member-header" id="requests">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/cloudfront/metrics.ts#L77">function <b>requests</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span>requests(change?: <a href='#CloudfrontMetricChange'>CloudfrontMetricChange</a>): <a href='/docs/reference/pkg/nodejs/pulumi/awsx/classic/cloudwatch/#Metric'>Metric</a></code></pre>


The number of requests for all HTTP methods and for both HTTP and HTTPS requests.

Valid Statistics: Sum
Units: None

<h4 class="pdoc-member-header" id="totalErrorRate">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/cloudfront/metrics.ts#L107">function <b>totalErrorRate</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span>totalErrorRate(change?: <a href='#CloudfrontMetricChange'>CloudfrontMetricChange</a>): <a href='/docs/reference/pkg/nodejs/pulumi/awsx/classic/cloudwatch/#Metric'>Metric</a></code></pre>


The percentage of all requests for which the HTTP status code is 4xx or 5xx.

Valid Statistics: Average
Units: Percent
