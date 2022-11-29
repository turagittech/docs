---
title: "Module classic/s3"
title_tag: "Module classic/s3 | Package @pulumi/awsx | Node.js SDK"
linktitle: "s3"
meta_desc: "Explore members of the s3 module in the @pulumi/awsx package."
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
    <a href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/s3/metrics.ts#L20">
        namespace <strong>metrics</strong>
    </a>
</h3>

<h4 class="pdoc-member-header" id="allRequests">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/s3/metrics.ts#L240">function <b>allRequests</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span>allRequests(change?: <a href='#S3MetricChange'>S3MetricChange</a>): <a href='/docs/reference/pkg/nodejs/pulumi/awsx/classic/cloudwatch/#Metric'>Metric</a></code></pre>


The total number of HTTP requests made to an Amazon S3 bucket, regardless of type. If you're
using a metrics configuration with a filter, then this metric only returns the HTTP requests
made to the objects in the bucket that meet the filter's requirements.

Units: Count

Valid statistics: Sum

<h4 class="pdoc-member-header" id="bucketSizeBytes">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/s3/metrics.ts#L213">function <b>bucketSizeBytes</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span>bucketSizeBytes(change?: <a href='#S3MetricChange'>S3MetricChange</a>): <a href='/docs/reference/pkg/nodejs/pulumi/awsx/classic/cloudwatch/#Metric'>Metric</a></code></pre>


The amount of data in bytes stored in a bucket in the STANDARD storage class,
INTELLIGENT_TIERING storage class, Standard - Infrequent Access (STANDARD_IA) storage class,
OneZone - Infrequent Access (ONEZONE_IA), Reduced Redundancy Storage (RRS) class, or Glacier
(GLACIER) storage class. This value is calculated by summing the size of all objects in the
bucket (both current and noncurrent objects), including the size of all parts for all
incomplete multipart uploads to the bucket.

Units: Bytes

Valid statistics: Average

<h4 class="pdoc-member-header" id="bytesDownloaded">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/s3/metrics.ts#L363">function <b>bytesDownloaded</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span>bytesDownloaded(change?: <a href='#S3MetricChange'>S3MetricChange</a>): <a href='/docs/reference/pkg/nodejs/pulumi/awsx/classic/cloudwatch/#Metric'>Metric</a></code></pre>


The number bytes downloaded for requests made to an Amazon S3 bucket, where the response
includes a body.

Units: Bytes

Valid statistics: Average (bytes per request), Sum (bytes per period), Sample Count, Min, Max

<h4 class="pdoc-member-header" id="bytesUploaded">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/s3/metrics.ts#L374">function <b>bytesUploaded</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span>bytesUploaded(change?: <a href='#S3MetricChange'>S3MetricChange</a>): <a href='/docs/reference/pkg/nodejs/pulumi/awsx/classic/cloudwatch/#Metric'>Metric</a></code></pre>


The number bytes uploaded that contain a request body, made to an Amazon S3 bucket.

Units: Bytes

Valid statistics: Average (bytes per request), Sum (bytes per period), Sample Count, Min, Max

<h4 class="pdoc-member-header" id="deleteRequests">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/s3/metrics.ts#L279">function <b>deleteRequests</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span>deleteRequests(change?: <a href='#S3MetricChange'>S3MetricChange</a>): <a href='/docs/reference/pkg/nodejs/pulumi/awsx/classic/cloudwatch/#Metric'>Metric</a></code></pre>


The number of HTTP DELETE requests made for objects in an Amazon S3 bucket. This also
includes Delete Multiple Objects requests. This metric shows the number of requests, not the
number of objects deleted.

Units: Count

Valid statistics: Sum

<h4 class="pdoc-member-header" id="errors4xx">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/s3/metrics.ts#L388">function <b>errors4xx</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span>errors4xx(change?: <a href='#S3MetricChange'>S3MetricChange</a>): <a href='/docs/reference/pkg/nodejs/pulumi/awsx/classic/cloudwatch/#Metric'>Metric</a></code></pre>


he number of HTTP 4xx client error status code requests made to an Amazon S3 bucket with a
value of either 0 or 1. The average statistic shows the error rate, and the sum statistic
shows the count of that type of error, during each period.

Units: Count

Valid statistics: Average (reports per request), Sum (reports per period), Min, Max, Sample
Count

<h4 class="pdoc-member-header" id="errors5xx">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/s3/metrics.ts#L402">function <b>errors5xx</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span>errors5xx(change?: <a href='#S3MetricChange'>S3MetricChange</a>): <a href='/docs/reference/pkg/nodejs/pulumi/awsx/classic/cloudwatch/#Metric'>Metric</a></code></pre>


The number of HTTP 5xx server error status code requests made to an Amazon S3 bucket with a
value of either 0 or 1. The average statistic shows the error rate, and the sum statistic
shows the count of that type of error, during each period.

Units: Count

Valid statistics: Average (reports per request), Sum (reports per period), Min, Max, Sample
Count

<h4 class="pdoc-member-header" id="firstByteLatency">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/s3/metrics.ts#L414">function <b>firstByteLatency</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span>firstByteLatency(change?: <a href='#S3MetricChange'>S3MetricChange</a>): <a href='/docs/reference/pkg/nodejs/pulumi/awsx/classic/cloudwatch/#Metric'>Metric</a></code></pre>


The per-request time from the complete request being received by an Amazon S3 bucket to when
the response starts to be returned.

Units: Milliseconds

Valid statistics: Average, Sum, Min, Max, Sample Count

<h4 class="pdoc-member-header" id="getRequests">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/s3/metrics.ts#L255">function <b>getRequests</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span>getRequests(change?: <a href='#S3MetricChange'>S3MetricChange</a>): <a href='/docs/reference/pkg/nodejs/pulumi/awsx/classic/cloudwatch/#Metric'>Metric</a></code></pre>


The number of HTTP GET requests made for objects in an Amazon S3 bucket. This doesn't include
list operations.

Note: Paginated list-oriented requests, like List Multipart Uploads, List Parts, Get Bucket
Object versions, and others, are not included in this metric.

Units: Count

Valid statistics: Sum

<h4 class="pdoc-member-header" id="headRequests">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/s3/metrics.ts#L290">function <b>headRequests</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span>headRequests(change?: <a href='#S3MetricChange'>S3MetricChange</a>): <a href='/docs/reference/pkg/nodejs/pulumi/awsx/classic/cloudwatch/#Metric'>Metric</a></code></pre>


The number of HTTP HEAD requests made to an Amazon S3 bucket.

Units: Count

Valid statistics: Sum

<h4 class="pdoc-member-header" id="listRequests">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/s3/metrics.ts#L351">function <b>listRequests</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span>listRequests(change?: <a href='#S3MetricChange'>S3MetricChange</a>): <a href='/docs/reference/pkg/nodejs/pulumi/awsx/classic/cloudwatch/#Metric'>Metric</a></code></pre>


The number of HTTP requests that list the contents of a bucket.

Units: Count

Valid statistics: Sum

<h4 class="pdoc-member-header" id="metric">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/s3/metrics.ts#L180">function <b>metric</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span>metric(metricName: <a href='#S3MetricName'>S3MetricName</a>, change: <a href='#S3MetricChange'>S3MetricChange</a>): <a href='/docs/reference/pkg/nodejs/pulumi/awsx/classic/cloudwatch/#Metric'>Metric</a></code></pre>


Creates an AWS/S3 metric with the requested [metricName]. See
https://docs.aws.amazon.com/AmazonS3/latest/dev/cloudwatch-monitoring.html for list of all
metric-names.

Note, individual metrics can easily be obtained without supplying the name using the other
[metricXXX] functions.

Amazon CloudWatch metrics for Amazon S3 can help you understand and improve the performance
of applications that use Amazon S3. There are two ways that you can use CloudWatch with
Amazon S3.

Daily Storage Metrics for Buckets ‐ You can monitor bucket storage using CloudWatch, which
collects and processes storage data from Amazon S3 into readable, daily metrics. These
storage metrics for Amazon S3 are reported once per day and are provided to all customers at
no additional cost.

Request metrics ‐ You can choose to monitor Amazon S3 requests to quickly identify and act on
operational issues. The metrics are available at 1 minute intervals after some latency to
process. These CloudWatch metrics are billed at the same rate as the Amazon CloudWatch Custom
Metrics. For information on CloudWatch pricing, see Amazon CloudWatch Pricing. To learn more
about how to opt-in to getting these metrics, see Metrics Configurations for Buckets.

When enabled, request metrics are reported for all object operations. By default, these
1-minute metrics are available at the Amazon S3 bucket level. You can also define a filter
for the metrics collected –using a shared prefix or object tag– allowing you to align metrics
filters to specific business applications, workflows, or internal organizations.

The following dimensions are used to filter Amazon S3 metrics:

1. "BucketName": This dimension filters the data you request for the identified bucket only.
2. "StorageType": This dimension filters the data that you have stored in a bucket by the
   following types of storage:

  * StandardStorage - The number of bytes used for objects in the STANDARD storage class.
  * IntelligentTieringFAStorage - The number of bytes used for objects in the Frequent Access
    tier of INTELLIGENT_TIERING storage class.
  * IntelligentTieringIAStorage - The number of bytes used for objects in the Infrequent
    Access tier of INTELLIGENT_TIERING storage class.
  * StandardIAStorage - The number of bytes used for objects in the Standard - Infrequent
    Access (STANDARD_IA) storage class.
  * StandardIASizeOverhead - The number of bytes used for objects smaller than 128 KB in size
    in the STANDARD_IA storage class.
  * OneZoneIAStorage - The number of bytes used for objects in the OneZone - Infrequent
    Access (ONEZONE_IA) storage class.
  * OneZoneIASizeOverhead - The number of bytes used for objects smaller than 128 KB in size
    in the ONEZONE_IA storage class.
  * ReducedRedundancyStorage - The number of bytes used for objects in the Reduced Redundancy
    Storage (RRS) class.
  * GlacierStorage - The number of bytes used for objects in the Glacier (GLACIER) storage
    class.
  * GlacierStorageOverhead - For each object archived to Glacier, Amazon S3 uses 8 KB of
    storage for the name of the object and other metadata. You are charged standard Amazon S3
    rates for this additional storage. For each archived object, Glacier adds 32 KB of
    storage for index and related metadata. This extra data is necessary to identify and
    restore your object. You are charged Glacier rates for this additional storage.

3. "FilterId": This dimension filters metrics configurations that you specify for request
   metrics on a bucket, for example, a prefix or a tag. You specify a filter id when you
   create a metrics configuration. For more information, see
   [Metrics-Configurations-for-Buckets](https://docs.aws.amazon.com/AmazonS3/latest/dev/metrics-configurations.html).

<h4 class="pdoc-member-header" id="numberOfObjects">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/s3/metrics.ts#L227">function <b>numberOfObjects</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span>numberOfObjects(change?: <a href='#S3MetricChange'>S3MetricChange</a>): <a href='/docs/reference/pkg/nodejs/pulumi/awsx/classic/cloudwatch/#Metric'>Metric</a></code></pre>


The total number of objects stored in a bucket for all storage classes except for the GLACIER
storage class. This value is calculated by counting all objects in the bucket (both current
and noncurrent objects) and the total number of parts for all incomplete multipart uploads to
the bucket.

Units: Count

Valid statistics: Average

<h4 class="pdoc-member-header" id="postRequests">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/s3/metrics.ts#L304">function <b>postRequests</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span>postRequests(change?: <a href='#S3MetricChange'>S3MetricChange</a>): <a href='/docs/reference/pkg/nodejs/pulumi/awsx/classic/cloudwatch/#Metric'>Metric</a></code></pre>


The number of HTTP POST requests made to an Amazon S3 bucket.

Note: Delete Multiple Objects and SELECT Object Content requests are not included in this
metric.

Units: Count

Valid statistics: Sum

<h4 class="pdoc-member-header" id="putRequests">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/s3/metrics.ts#L266">function <b>putRequests</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span>putRequests(change?: <a href='#S3MetricChange'>S3MetricChange</a>): <a href='/docs/reference/pkg/nodejs/pulumi/awsx/classic/cloudwatch/#Metric'>Metric</a></code></pre>


The number of HTTP PUT requests made for objects in an Amazon S3 bucket.

Units: Count

Valid statistics: Sum

<h4 class="pdoc-member-header" id="S3MetricChange">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/s3/metrics.ts#L29">interface <b>S3MetricChange</b></a>
</h4>

<pre class="highlight"><code><span class='kr'>interface</span> <span class='nx'>S3MetricChange</span> <span class='kr'>extends</span> <a href='/docs/reference/pkg/nodejs/pulumi/awsx/classic/cloudwatch/#MetricChange'>MetricChange</a></code></pre>
<h4 class="pdoc-member-header" id="S3MetricChange-bucket">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/s3/metrics.ts#L33">property <b>bucket</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>bucket?: <a href='/docs/reference/pkg/nodejs/pulumi/aws/s3/#Bucket'>aws.s3.Bucket</a>;</code></pre>

Optional bucket to filter metrics down to.

<h4 class="pdoc-member-header" id="S3MetricChange-color">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/cloudwatch/metric.ts#L464">property <b>color</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>color?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

The six-digit HTML hex color code to be used for this metric.

Only used if this metric is displayed in a [Dashboard] with a [MetricWidget].

<h4 class="pdoc-member-header" id="S3MetricChange-dimensions">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/cloudwatch/metric.ts#L433">property <b>dimensions</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>dimensions?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;Record&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;&gt;&gt;;</code></pre>

The new dimension for this metric.  If this object is missing this property, then no change
will be made.  However, if the property is there by set to [undefined] then the value will be
cleared.

<h4 class="pdoc-member-header" id="S3MetricChange-extendedStatistic">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/cloudwatch/metric.ts#L451">property <b>extendedStatistic</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>extendedStatistic?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number'>number</a></span>&gt;;</code></pre>

The new percentile statistic for the metric associated with the alarm.  If this object is
missing this property, then no change will be made.  However, if the property is there by set
to [undefined] then the value will be set to the default.

<h4 class="pdoc-member-header" id="S3MetricChange-filterId">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/s3/metrics.ts#L115">property <b>filterId</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>filterId?: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</code></pre>

This dimension filters metrics configurations that you specify for request metrics on a
bucket, for example, a prefix or a tag. You specify a filter id when you create a metrics
configuration. For more information, see
[Metrics-Configurations-for-Buckets](https://docs.aws.amazon.com/AmazonS3/latest/dev/metrics-configurations.html).

<h4 class="pdoc-member-header" id="S3MetricChange-label">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/cloudwatch/metric.ts#L473">property <b>label</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>label?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

The label to display for this metric in the graph legend. If this is not specified, the
metric is given an autogenerated label that distinguishes it from the other metrics in the
widget.

Only used if this metric is displayed in a [Dashboard] with a [MetricWidget].

<h4 class="pdoc-member-header" id="S3MetricChange-period">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/cloudwatch/metric.ts#L439">property <b>period</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>period?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number'>number</a></span>&gt;;</code></pre>

The new period in seconds over which the specified `stat` is applied.  If this object is
missing this property, then no change will be made.  However, if the property is there by set
to [undefined] then the value will be set to the default (300s).

<h4 class="pdoc-member-header" id="S3MetricChange-statistic">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/cloudwatch/metric.ts#L445">property <b>statistic</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>statistic?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/awsx/classic/cloudwatch/#MetricStatistic'>MetricStatistic</a>&gt;;</code></pre>

The new statistic to apply to the alarm's associated metric.  If this object is missing this
property, then no change will be made.  However, if the property is there by set to
[undefined] then the value will be set to the default.

<h4 class="pdoc-member-header" id="S3MetricChange-storageType">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/s3/metrics.ts#L101">property <b>storageType</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>storageType?: <span class='s2'>"StandardStorage"</span> | <span class='s2'>"IntelligentTieringAAStorage"</span> | <span class='s2'>"IntelligentTieringDAAStorage"</span> | <span class='s2'>"IntelligentTieringFAStorage"</span> | <span class='s2'>"IntelligentTieringIAStorage"</span> | <span class='s2'>"StandardIAStorage"</span> | <span class='s2'>"StandardIASizeOverhead"</span> | <span class='s2'>"IntAAObjectOverhead"</span> | <span class='s2'>"IntAAS3ObjectOverhead"</span> | <span class='s2'>"IntDAAObjectOverhead"</span> | <span class='s2'>"IntDAAS3ObjectOverhead"</span> | <span class='s2'>"OneZoneIAStorage"</span> | <span class='s2'>"OneZoneIASizeOverhead"</span> | <span class='s2'>"ReducedRedundancyStorage"</span> | <span class='s2'>"GlacierStorage"</span> | <span class='s2'>"GlacierStagingStorage"</span> | <span class='s2'>"GlacierObjectOverhead"</span> | <span class='s2'>"GlacierS3ObjectOverhead"</span> | <span class='s2'>"DeepArchiveStorage"</span> | <span class='s2'>"DeepArchiveObjectOverhead"</span> | <span class='s2'>"DeepArchiveS3ObjectOverhead"</span> | <span class='s2'>"DeepArchiveStagingStorage"</span> | <span class='s2'>"AllStorageTypes"</span>;</code></pre>

This dimension filters the data that you have stored in a bucket by the following types
of storage:

* StandardStorage - The number of bytes used for objects in the STANDARD storage class.
* IntelligentTieringAAStorage - The number of bytes used for objects in the Archive
  Access tier of INTELLIGENT_TIERING storage class.
* IntelligentTieringDAAStorage - The number of bytes used for objects in the Deep
  Archive Access tier of INTELLIGENT_TIERING storage class.
* IntelligentTieringFAStorage - The number of bytes used for objects in the Frequent
  Access tier of INTELLIGENT_TIERING storage class.
* IntelligentTieringIAStorage - The number of bytes used for objects in the Infrequent
  Access tier of INTELLIGENT_TIERING storage class.
* StandardIAStorage - The number of bytes used for objects in the Standard-Infrequent
  Access (STANDARD_IA) storage class. This extra data is necessary to identify and
  restore your object. You are charged GLACIER rates for this additional storage.
* StandardIASizeOverhead - The number of bytes used for objects smaller than 128 KB in
  size in the STANDARD_IA storage class.
* IntAAObjectOverhead - For each object in INTELLIGENT_TIERING storage class in the
  Archive Access tier, GLACIER adds 32 KB of storage for index and related metadata.
  This extra data is necessary to identify and restore your object. You are charged
  GLACIER rates for this additional storage.
* IntAAS3ObjectOverhead - For each object in INTELLIGENT_TIERING storage class in the
  Archive Access tier, Amazon S3 uses 8 KB of storage for the name of the object and
  other metadata. You are charged STANDARD rates for this additional storage.
* IntDAAObjectOverhead - For each object in INTELLIGENT_TIERING storage class in the
  Deep Archive Access tier, GLACIER adds 32 KB of storage for index and related
  metadata. This extra data is necessary to identify and restore your object. You are
  charged S3 Glacier Deep Archive storage rates for this additional storage.
* IntDAAS3ObjectOverhead - For each object in INTELLIGENT_TIERING storage class in the
  Deep Archive Access tier, Amazon S3 adds 8 KB of storage for index and related
  metadata. This extra data is necessary to identify and restore your object. You are
  charged STANDARD rates for this additional storage.
* OneZoneIAStorage - The number of bytes used for objects in the OneZone-Infrequent
  Access (ONEZONE_IA) storage class.
* OneZoneIASizeOverhead - The number of bytes used for objects smaller than 128 KB in
  size in the ONEZONE_IA storage class.
* ReducedRedundancyStorage - The number of bytes used for objects in the Reduced
  Redundancy Storage (RRS) class.
* GlacierStorage - The number of bytes used for objects in the GLACIER storage class.
* GlacierStagingStorage - The number of bytes used for parts of Multipart objects
  before the CompleteMultipartUpload request is completed on objects in the GLACIER
  storage class.
* GlacierObjectOverhead - For each archived object, GLACIER adds 32 KB of storage for
  index and related metadata. This extra data is necessary to identify and restore
  your object. You are charged GLACIER rates for this additional storage.
* GlacierS3ObjectOverhead - For each object archived to GLACIER , Amazon S3 uses 8 KB
  of storage for the name of the object and other metadata. You are charged STANDARD
  rates for this additional storage.
* DeepArchiveStorage - The number of bytes used for objects in the S3 Glacier Deep
  Archive storage class.
* DeepArchiveObjectOverhead - For each archived object, S3 Glacier Deep Archive adds
  32 KB of storage for index and related metadata. This extra data is necessary to
  identify and restore your object. You are charged S3 Glacier Deep Archive rates
  for this additional storage.
* DeepArchiveS3ObjectOverhead - For each object archived to S3 Glacier Deep Archive,
  Amazon S3 uses 8 KB of storage for the name of the object and other metadata. You
  are charged STANDARD rates for this additional storage.
* DeepArchiveStagingStorage – The number of bytes used for parts of Multipart objects
  before the CompleteMultipartUpload request is completed on objects in the S3
  Glacier Deep Archive storage class.
* AllStorageTypes - All available storage types, used by NumberOfObjects metric

For more information, see
[Metrics-and-dimensions](https://docs.aws.amazon.com/AmazonS3/latest/userguide/metrics-dimensions.html).

<h4 class="pdoc-member-header" id="S3MetricChange-unit">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/cloudwatch/metric.ts#L457">property <b>unit</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>unit?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/awsx/classic/cloudwatch/#MetricUnit'>MetricUnit</a>&gt;;</code></pre>

The new unit for this metric.   If this object is missing this property, then no change will
be made.  However, if the property is there by set to [undefined] then the value will be set
to the default.

<h4 class="pdoc-member-header" id="S3MetricChange-visible">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/cloudwatch/metric.ts#L481">property <b>visible</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>visible?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean'>boolean</a></span>&gt;;</code></pre>

Set this to true to have the metric appear in the graph, or false to have it be hidden. The
default is true.

Only used if this metric is displayed in a [Dashboard] with a [MetricWidget].

<h4 class="pdoc-member-header" id="S3MetricChange-yAxis">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/cloudwatch/metric.ts#L488">property <b>yAxis</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>yAxis?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='s2'>"left"</span> | <span class='s2'>"right"</span>&gt;;</code></pre>

Where on the graph to display the y-axis for this metric. The default is left.

Only used if this metric is displayed in a [Dashboard] with a [MetricWidget].

<h4 class="pdoc-member-header" id="S3MetricName">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/s3/metrics.ts#L21">type <b>S3MetricName</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>type</span> S3MetricName = <span class='s2'>"BucketSizeBytes"</span> | <span class='s2'>"NumberOfObjects"</span> | <span class='s2'>"AllRequests"</span> | <span class='s2'>"GetRequests"</span> | <span class='s2'>"PutRequests"</span> | <span class='s2'>"DeleteRequests"</span> | <span class='s2'>"HeadRequests"</span> | <span class='s2'>"PostRequests"</span> | <span class='s2'>"SelectRequests"</span> | <span class='s2'>"SelectScannedBytes"</span> | <span class='s2'>"SelectReturnedBytes"</span> | <span class='s2'>"ListRequests"</span> | <span class='s2'>"BytesDownloaded"</span> | <span class='s2'>"BytesUploaded"</span> | <span class='s2'>"4xxErrors"</span> | <span class='s2'>"5xxErrors"</span> | <span class='s2'>"FirstByteLatency"</span> | <span class='s2'>"TotalRequestLatency"</span>;</code></pre>
<h4 class="pdoc-member-header" id="selectRequests">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/s3/metrics.ts#L316">function <b>selectRequests</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span>selectRequests(change?: <a href='#S3MetricChange'>S3MetricChange</a>): <a href='/docs/reference/pkg/nodejs/pulumi/awsx/classic/cloudwatch/#Metric'>Metric</a></code></pre>


The number of Amazon S3 SELECT Object Content requests made for objects in an Amazon S3
bucket.

Units: Count

Valid statistics: Sum

<h4 class="pdoc-member-header" id="selectReturnedBytes">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/s3/metrics.ts#L340">function <b>selectReturnedBytes</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span>selectReturnedBytes(change?: <a href='#S3MetricChange'>S3MetricChange</a>): <a href='/docs/reference/pkg/nodejs/pulumi/awsx/classic/cloudwatch/#Metric'>Metric</a></code></pre>


The number of bytes of data returned with Amazon S3 SELECT Object Content requests in an
Amazon S3 bucket.

Units: Bytes

Valid statistics: Average (bytes per request), Sum (bytes per period), Sample Count, Min, Max

<h4 class="pdoc-member-header" id="selectScannedBytes">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/s3/metrics.ts#L328">function <b>selectScannedBytes</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span>selectScannedBytes(change?: <a href='#S3MetricChange'>S3MetricChange</a>): <a href='/docs/reference/pkg/nodejs/pulumi/awsx/classic/cloudwatch/#Metric'>Metric</a></code></pre>


The number of bytes of data scanned with Amazon S3 SELECT Object Content requests in an
Amazon S3 bucket.

Units: Bytes

Valid statistics: Average (bytes per request), Sum (bytes per period), Sample Count, Min, Max

<h4 class="pdoc-member-header" id="totalRequestLatency">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-awsx/blob/43b8dabc0ec1e5187bf63e107bf06ee54021a1a7/sdk/nodejs/classic/s3/metrics.ts#L427">function <b>totalRequestLatency</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span>totalRequestLatency(change?: <a href='#S3MetricChange'>S3MetricChange</a>): <a href='/docs/reference/pkg/nodejs/pulumi/awsx/classic/cloudwatch/#Metric'>Metric</a></code></pre>


The elapsed per-request time from the first byte received to the last byte sent to an Amazon
S3 bucket. This includes the time taken to receive the request body and send the response
body, which is not included in FirstByteLatency.

Units: Milliseconds

Valid statistics: Average, Sum, Min, Max, Sample Count
