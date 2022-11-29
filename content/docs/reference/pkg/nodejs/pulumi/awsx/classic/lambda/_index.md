---
title: "Module classic/lambda"
title_tag: "Module classic/lambda | Package @pulumi/awsx | Node.js SDK"
linktitle: "lambda"
meta_desc: "Explore members of the lambda module in the @pulumi/awsx package."
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
    <a href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/lambda/metrics.ts#L20">
        namespace <strong>metrics</strong>
    </a>
</h3>

<h4 class="pdoc-member-header" id="concurrentExecutions">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/lambda/metrics.ts#L174">function <b>concurrentExecutions</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span>concurrentExecutions(change?: <a href='#LambdaMetricChange'>LambdaMetricChange</a>): <a href='/docs/reference/pkg/nodejs/pulumi/awsx/classic/cloudwatch/#Metric'>Metric</a></code></pre>


Emitted as an aggregate metric for all functions in the account, and for functions that have
a custom concurrency limit specified. Not applicable for versions or aliases. Measures the
sum of concurrent executions for a given function at a given point in time. Must be viewed as
an average metric if aggregated across a time period.

Units: Count

<h4 class="pdoc-member-header" id="deadLetterErrors">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/lambda/metrics.ts#L126">function <b>deadLetterErrors</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span>deadLetterErrors(change?: <a href='#LambdaMetricChange'>LambdaMetricChange</a>): <a href='/docs/reference/pkg/nodejs/pulumi/awsx/classic/cloudwatch/#Metric'>Metric</a></code></pre>


Incremented when Lambda is unable to write the failed event payload to your configured Dead
Letter Queues. This could be due to the following:

* Permissions errors
* Throttles from downstream services
* Misconfigured resources
* Timeouts

Units: Count

<h4 class="pdoc-member-header" id="duration">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/lambda/metrics.ts#L139">function <b>duration</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span>duration(change?: <a href='#LambdaMetricChange'>LambdaMetricChange</a>): <a href='/docs/reference/pkg/nodejs/pulumi/awsx/classic/cloudwatch/#Metric'>Metric</a></code></pre>


Measures the elapsed wall clock time from when the function code starts executing as a result
of an invocation to when it stops executing. The maximum data point value possible is the
function timeout configuration. The billed duration will be rounded up to the nearest 100
millisecond. Note that AWS Lambda only sends these metrics to CloudWatch if they have a
nonzero value.

Units: Count

<h4 class="pdoc-member-header" id="errors">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/lambda/metrics.ts#L111">function <b>errors</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span>errors(change?: <a href='#LambdaMetricChange'>LambdaMetricChange</a>): <a href='/docs/reference/pkg/nodejs/pulumi/awsx/classic/cloudwatch/#Metric'>Metric</a></code></pre>


Measures the number of invocations that failed due to errors in the function (response code
4XX). This replaces the deprecated ErrorCount metric. Failed invocations may trigger a retry
attempt that succeeds. This includes:

* Handled exceptions (for example, context.fail(error))
* Unhandled exceptions causing the code to exit
* Out of memory exceptions
* Timeouts
* Permissions errors

This does not include invocations that fail due to invocation rates exceeding default
concurrent limits (error code 429) or failures due to internal service errors (error code
500).

Units: Count

<h4 class="pdoc-member-header" id="invocations">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/lambda/metrics.ts#L90">function <b>invocations</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span>invocations(change?: <a href='#LambdaMetricChange'>LambdaMetricChange</a>): <a href='/docs/reference/pkg/nodejs/pulumi/awsx/classic/cloudwatch/#Metric'>Metric</a></code></pre>


Measures the number of times a function is invoked in response to an event or invocation API
call. This replaces the deprecated RequestCount metric. This includes successful and failed
invocations, but does not include throttled attempts. This equals the billed requests for the
function. Note that AWS Lambda only sends these metrics to CloudWatch if they have a nonzero
value.

Units: Count

<h4 class="pdoc-member-header" id="iteratorAge">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/lambda/metrics.ts#L162">function <b>iteratorAge</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span>iteratorAge(change?: <a href='#LambdaMetricChange'>LambdaMetricChange</a>): <a href='/docs/reference/pkg/nodejs/pulumi/awsx/classic/cloudwatch/#Metric'>Metric</a></code></pre>


Emitted for stream-based invocations only (functions triggered by an Amazon DynamoDB stream
or Kinesis stream). Measures the age of the last record for each batch of records processed.
Age is the difference between the time Lambda received the batch, and the time the last
record in the batch was written to the stream.

Units: Milliseconds

<h4 class="pdoc-member-header" id="LambdaMetricChange">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/lambda/metrics.ts#L25">interface <b>LambdaMetricChange</b></a>
</h4>

<pre class="highlight"><code><span class='kr'>interface</span> <span class='nx'>LambdaMetricChange</span> <span class='kr'>extends</span> <a href='/docs/reference/pkg/nodejs/pulumi/awsx/classic/cloudwatch/#MetricChange'>MetricChange</a></code></pre>
<h4 class="pdoc-member-header" id="LambdaMetricChange-color">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/cloudwatch/metric.ts#L464">property <b>color</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>color?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

The six-digit HTML hex color code to be used for this metric.

Only used if this metric is displayed in a [Dashboard] with a [MetricWidget].

<h4 class="pdoc-member-header" id="LambdaMetricChange-dimensions">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/cloudwatch/metric.ts#L433">property <b>dimensions</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>dimensions?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;Record&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;&gt;&gt;;</code></pre>

The new dimension for this metric.  If this object is missing this property, then no change
will be made.  However, if the property is there by set to [undefined] then the value will be
cleared.

<h4 class="pdoc-member-header" id="LambdaMetricChange-executedVersion">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/lambda/metrics.ts#L40">property <b>executedVersion</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>executedVersion?: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</code></pre>

Filters the metric data by Lambda function versions. This only applies to alias
invocations.

<h4 class="pdoc-member-header" id="LambdaMetricChange-extendedStatistic">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/cloudwatch/metric.ts#L451">property <b>extendedStatistic</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>extendedStatistic?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number'>number</a></span>&gt;;</code></pre>

The new percentile statistic for the metric associated with the alarm.  If this object is
missing this property, then no change will be made.  However, if the property is there by set
to [undefined] then the value will be set to the default.

<h4 class="pdoc-member-header" id="LambdaMetricChange-function">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/lambda/metrics.ts#L29">property <b>function</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>function?: <a href='/docs/reference/pkg/nodejs/pulumi/aws/lambda/#Function'>aws.lambda.Function</a>;</code></pre>

Optional Function this metric should be filtered down to.

<h4 class="pdoc-member-header" id="LambdaMetricChange-label">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/cloudwatch/metric.ts#L473">property <b>label</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>label?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

The label to display for this metric in the graph legend. If this is not specified, the
metric is given an autogenerated label that distinguishes it from the other metrics in the
widget.

Only used if this metric is displayed in a [Dashboard] with a [MetricWidget].

<h4 class="pdoc-member-header" id="LambdaMetricChange-period">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/cloudwatch/metric.ts#L439">property <b>period</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>period?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number'>number</a></span>&gt;;</code></pre>

The new period in seconds over which the specified `stat` is applied.  If this object is
missing this property, then no change will be made.  However, if the property is there by set
to [undefined] then the value will be set to the default (300s).

<h4 class="pdoc-member-header" id="LambdaMetricChange-resource">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/lambda/metrics.ts#L34">property <b>resource</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>resource?: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</code></pre>

Filters the metric data by Lambda function resource, such as function version or alias.

<h4 class="pdoc-member-header" id="LambdaMetricChange-statistic">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/cloudwatch/metric.ts#L445">property <b>statistic</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>statistic?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/awsx/classic/cloudwatch/#MetricStatistic'>MetricStatistic</a>&gt;;</code></pre>

The new statistic to apply to the alarm's associated metric.  If this object is missing this
property, then no change will be made.  However, if the property is there by set to
[undefined] then the value will be set to the default.

<h4 class="pdoc-member-header" id="LambdaMetricChange-unit">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/cloudwatch/metric.ts#L457">property <b>unit</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>unit?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/awsx/classic/cloudwatch/#MetricUnit'>MetricUnit</a>&gt;;</code></pre>

The new unit for this metric.   If this object is missing this property, then no change will
be made.  However, if the property is there by set to [undefined] then the value will be set
to the default.

<h4 class="pdoc-member-header" id="LambdaMetricChange-visible">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/cloudwatch/metric.ts#L481">property <b>visible</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>visible?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean'>boolean</a></span>&gt;;</code></pre>

Set this to true to have the metric appear in the graph, or false to have it be hidden. The
default is true.

Only used if this metric is displayed in a [Dashboard] with a [MetricWidget].

<h4 class="pdoc-member-header" id="LambdaMetricChange-yAxis">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/cloudwatch/metric.ts#L488">property <b>yAxis</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>yAxis?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='s2'>"left"</span> | <span class='s2'>"right"</span>&gt;;</code></pre>

Where on the graph to display the y-axis for this metric. The default is left.

Only used if this metric is displayed in a [Dashboard] with a [MetricWidget].

<h4 class="pdoc-member-header" id="LambdaMetricName">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/lambda/metrics.ts#L21">type <b>LambdaMetricName</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>type</span> LambdaMetricName = <span class='s2'>"Invocations"</span> | <span class='s2'>"Errors"</span> | <span class='s2'>"DeadLetterErrors"</span> | <span class='s2'>"Duration"</span> | <span class='s2'>"Throttles"</span> | <span class='s2'>"IteratorAge"</span> | <span class='s2'>"ConcurrentExecutions"</span> | <span class='s2'>"UnreservedConcurrentExecutions"</span>;</code></pre>
<h4 class="pdoc-member-header" id="metric">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/lambda/metrics.ts#L60">function <b>metric</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span>metric(metricName: <a href='#LambdaMetricName'>LambdaMetricName</a>, change: <a href='#LambdaMetricChange'>LambdaMetricChange</a>): <a href='/docs/reference/pkg/nodejs/pulumi/awsx/classic/cloudwatch/#Metric'>Metric</a></code></pre>


Creates an AWS/Lambda metric with the requested [metricName]. See
https://docs.aws.amazon.com/lambda/latest/dg/monitoring-functions-metrics.html for list of
all metric-names.

Note, individual metrics can easily be obtained without supplying the name using the other
[metricXXX] functions.

You can use the following dimensions to refine the metrics returned for your Lambda
functions:

1. "FunctionName". Filters the metric data by Lambda function.
2. "Resource". Filters the metric data by Lambda function resource, such as function version
   or alias.
3. "ExecutedVersion". Filters the metric data by Lambda function versions. This only applies
   to alias invocations.

<h4 class="pdoc-member-header" id="throttles">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/lambda/metrics.ts#L150">function <b>throttles</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span>throttles(change?: <a href='#LambdaMetricChange'>LambdaMetricChange</a>): <a href='/docs/reference/pkg/nodejs/pulumi/awsx/classic/cloudwatch/#Metric'>Metric</a></code></pre>


Measures the number of Lambda function invocation attempts that were throttled due to
invocation rates exceeding the customer’s concurrent limits (error code 429). Failed
invocations may trigger a retry attempt that succeeds.

Units: Count

<h4 class="pdoc-member-header" id="unreservedConcurrentExecutions">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/lambda/metrics.ts#L186">function <b>unreservedConcurrentExecutions</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span>unreservedConcurrentExecutions(change?: <a href='#LambdaMetricChange'>LambdaMetricChange</a>): <a href='/docs/reference/pkg/nodejs/pulumi/awsx/classic/cloudwatch/#Metric'>Metric</a></code></pre>


Emitted as an aggregate metric for all functions in the account only. Not applicable for
functions, versions, or aliases. Represents the sum of the concurrency of the functions that
do not have a custom concurrency limit specified. Must be viewed as an average metric if
aggregated across a time period.

Units: Count
