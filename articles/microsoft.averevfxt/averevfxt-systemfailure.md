<properties
    pageTitle="Avere vFXT System Failure or Service Restart Issues"
    description="Resolve issues with Avere vFXT system failures or service restarts."
    infoBubbleText="Avere vFXT System Failure or Service Restart Issues"
    authors="jbut"
    ms.author="jebutl"
    displayOrder="1"
    articleId="averevfxt-systemfailure"
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32609696"
    resourceTags=""
    productPesIds="16506"
    cloudEnvironments="public, fairfax, usnat, ussec"
    ownershipId="StorageMediaEdge_AvereVFXT"
/>

# Avere vFXT System Failure or Service Restart Issues

Many system failure or service start issues may be solved by the following actions.

## *High Availability*

If an Avere vFXT node fails, the high availability (HA) protection will ensure that another node takes over for that failed node.  A common scenario involves transient failures.  A node may experience a failure event, and the node's HA partner (secondary) node will take over for that temporarily failed nodes.  After the failed node recovers, the services will return to the original node.  Although clients will be transiently impacted, the system should automatically recover. You should wait 10-20 minutes to determine if the system automatically recovers.

## *Dashboard Alerts and Conditions*

When an Avere vFXT experiences a failure, the failure events will be logged via the Avere Control Panel alerts and conditions panes.  This view provides a stream of events that you can watch during a failure event.

You may check for alerts and/or conditions by navigating to the main page of the Avere Control Panel.  The conditions and alerts appear in tabs below the main graph.

[Monitoring Conditions and Alerts](https://azure.github.io/Avere/legacy/dashboard/4_7/html/dash_conditions_alerts.html) provides more details.

## *Uploading a Support Bundle*

Uploading a support bundle also involves accessing the Avere Control Panel. It is important to note that the support bundle will only be uploaded to Microsoft Support if you've taken the steps to configure support uploads. Follow these steps:

1. Navigate to the Support tab of the Avere Control Panel.
2. Go to the General information upload section and select the "Support bundle" mode.
3. Provide an optional comment to indicate what information is being gathered.
4. Click the "Upload Information" button.

[General Information Upload](https://azure.github.io/Avere/legacy/ops_guide/4_7/html/support_overview.html#general-information-upload) describes the Support Bundle upload process in more detail.

Please see [Enable support updates](https://docs.microsoft.com/azure/avere-vfxt/avere-vfxt-enable-support) for details on enabling support uploads.

## *Uploading a Core File*

Sometimes when file system services go offline, a process core file is written on the failing node. You may upload a core file by navigating to the Support tab on the Avere Control Panel.  From this page, go to the "Core dump management" section.  [Core Dump Management](https://azure.github.io/Avere/legacy/ops_guide/4_7/html/support_overview.html#core-dump-management) provides more detail on uploading core files.

## **Recommended Documents**

* [Cluster High Availability](https://azure.github.io/Avere/legacy/ops_guide/4_7/html/gui_ha.html)
* [Monitoring Conditions and Alerts](https://azure.github.io/Avere/legacy/dashboard/4_7/html/dash_conditions_alerts.html)
* [Using the Avere Control Panel Support Tab](https://azure.github.io/Avere/legacy/ops_guide/4_7/html/support_overview.html)


