<properties
    pageTitle="Avere vFXT Performance Issues"
    description="Resolve issues with Avere vFXT performance."
    infoBubbleText="Avere vFXT Performance Issues"
    authors="jbut"
    ms.author="jebutl"
    displayOrder="1"
    articleId="averevfxt-performance"
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32609694"
    resourceTags=""
    productPesIds="16506"
    cloudEnvironments="public, fairfax, usnat, ussec"
    ownershipId="StorageMediaEdge_AvereVFXT"
/>

# Avere vFXT Performance Issues

The following actions and considerations may help to address Avere vFXT performance issues.

## *Introduction*

Performance problems can arise for many reasons.  This information may help you sort out the root cause for the issues that you're seeing.

## *Conditions on the Avere Control Panel Dashboard*

If the Avere vFXT cluster is in an error state, that could very easily explain performance issues. For example, if the system is having problems communicating with a core filer, that may explain why it can't serve requests as fast as expected.

In order to determine what's potentially wrong, view the dashboard alerts and conditions.  Do this by viewing the main screen of the Avere Control Panel, and view the bottom section of the screen.  [Monitoring Conditions and Alerts](https://azure.github.io/Avere/legacy/dashboard/4_7/html/dash_conditions_alerts.html) describes this in more detail.

## *Moving data to the vFXT cluster*

The Avere vFXT is designed to manage very large datasets.  One of the big challenges is getting all data copied into a new filesystem.  [Moving data to the vFXT cluster - parallel data ingest](https://docs.microsoft.com/azure/avere-vfxt/avere-vfxt-data-ingest) provides a variety of techniques for speeding up this task.

## *Workload Properties*

Performance is largely a function of the workload that is being applied to an Avere vFXT cluster.  It is important to try to determine if the workload is from a single client and is single-threaded. By single-threaded, we mean a workload that involves a single process sending a single stream of operations to the file system server.  For example, a single invocation of a command like *ls* would send a series of file system operations, mainly READDIR+ for NFS, to a server to list directory contents.  On the other hand, one may invoke 10 copies of the *ls* program in parallel to quickly list different parts of a directory tree.  This would result in multiple streams of file system operations.  In general, single-stream workloads are bound by file system latency. A quick way of improving performance would be to make the workload more parallel or multi-threaded/multi-process.

In addition to using multiple processes on a single client, you may enlist multiple clients in your application.  Multiple clients bring more network and CPU resources to accomplish a task. If you think you're experiencing a single-client bottleneck, adding a client may be a good way to determine if you can get more throughput by adding clients.

## *Ability to Cache Data*

How much of your data set fits in the Avere cache?  If you have a workload that accesses a very large amount of data, then you may have limited performance due to cache misses.  You can determine your cache hit rates by examining the system dashboard on the Avere Control Panel.  Any access to the core filers will result in decreased performance levels.  If you notice cache misses, it may help to increase the number of nodes in your Avere vFXT cluster or increase the size of the disks attached to the Avere vFXT nodes.  [Viewing System Performance](https://azure.github.io/Avere/legacy/dashboard/4_7/html/dash_performance_graph.html) provides additional information regarding monitoring performance via the dashboard.  [Manage the Avere vFXT cluster](https://docs.microsoft.com/azure/avere-vfxt/avere-vfxt-manage-cluster) describes how to add nodes using the *vfxt.py* utility.

## *Setting up Support Uploads*

In order to diagnose performance problems, it is very helpful to have support uploads enabled.  Support uploads provide Microsoft Support with detailed telemetry regarding Avere vFXT cluster performance.  Please see [Enable support updates](https://docs.microsoft.com/azure/avere-vfxt/avere-vfxt-enable-support) for more information on this.

## *Uploading a Support Bundle*

Uploading Support Bundles immediately following performance issues is helpful in diagnosing problems.

Uploading a support bundle also involves accessing the Avere Control Panel. It is important to note, that the support bundle will only be uploaded to Microsoft Support if you've taken the steps to configure support uploads (See Setting up Support Uploads section above). Follow these steps:

1. Navigate to the Support tab of the Avere Control Panel.
2. Go to the General information upload section and select the "Support bundle" mode.
3. Provide an optional comment to indicate what information is being gathered.
4. Click the "Upload Information" button.

Please see [Enable support updates](https://docs.microsoft.com/azure/avere-vfxt/avere-vfxt-enable-support) for details on enabling support uploads.

## *Reproducing Problems and Baselining Performance*

It is very useful to have a baseline test to reproduce the performance problems that you're seeing.  Applications can be very complex, so having a simple model application can help to provide a reproducible scenario that can be used to study the performance problem.  Furthermore, if the reproducible scenario uses completely generic tools and data, then you may be able to share this reproduction with Microsoft Support to help resolve the performance issues.  You may also be able to compare this performance level to an expected baseline level of performance that is expected from the system.

## **Recommended Documents**

1. [Vdbench - measuring HPC cache or vFXT performance](https://github.com/Azure/Avere/blob/master/docs/vdbench.md)
2. [Cluster tuning](https://docs.microsoft.com/azure/avere-vfxt/avere-vfxt-tuning)
