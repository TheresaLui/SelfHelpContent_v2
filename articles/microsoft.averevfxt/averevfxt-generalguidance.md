<properties
    pageTitle="Avere vFXT General Guidance or Advisory"
    description="Resolve general issues with Avere vFXT cluster."
    infoBubbleText="Avere vFXT Cluster General Guidance or Advisory"
    authors="jbut"
    ms.author="jebutl"
    displayOrder="1"
    articleId="averevfxt-generalguidance"
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32626105,32609691"
    resourceTags=""
    productPesIds="16506"
    cloudEnvironments="public, fairfax, usnat, ussec"
    ownershipId="StorageMediaEdge_AvereVFXT"
/>

# Avere vFXT Cluster General Guidance or Advisory

The following advice may help with the problem that you're experiencing.

## *Key Actions*

Here are some key actions to take:

1. Check the Avere Control Panel Dashboard for alerts and/or conditions
2. Check the Dashboard graphs and note the time period of problems
3. Upload a Support Bundle from the Support Page of the Avere Control Panel

You may check for alerts and/or conditions by navigating to the main page of the Avere Control Panel. The conditions and alerts appear in tabs below the main graph.

Similarly, you may also check the Dashboard graphs by navigating to the main page of the Avere Control Panel.

Finally, uploading a support bundle also involves accessing the Avere Control Panel. It is important to note, that the support bundle will only be uploaded to Microsoft Support if you've taken the steps to configure support uploads. Follow these steps:

1. Navigate to the Support tab of the Avere Control Panel
2. Go to the General information upload section and select the "Support bundle" mode
3. Provide an optional comment to indicate what information is being gathered
4. Click the "Upload Information" button

Please see [Enable support updates](https://docs.microsoft.com/azure/avere-vfxt/avere-vfxt-enable-support) for details on enabling support uploads.

## *Restarting Services*

Sometimes it is helpful to restart services in order to resolve issues. A service restart may resolve issues when file system operations are not completing. You may restart services via the following steps:

1. Navigate to the Administration -> System Maintenance section of the Avere Control Panel
2. Determine whether you want to perform a high-availability (HA) restart or a non-HA restart. An HA restart minimizes the disruption to clients, but it may extend the overall amount of time that the operation will run. A non-HA restart is useful if you're not concerned about the impact on clients. HA restarts will restart services on one node at a time.
3. Click the "Restart cluster" button

[Restart Services Instructions](https://azure.github.io/Avere/legacy/ops_guide/4_7/html/gui_system_maintenance.html) provides more details on restarting services.

## **Recommended Documents**

You may find documentation for the Avere vFXT on the Microsoft documentation site.  The following links provide key resources:

* [Viewing System Performance](https://azure.github.io/Avere/legacy/dashboard/4_7/html/dash_performance_graph.html)
* [Monitoring Conditions and Alerts](https://azure.github.io/Avere/legacy/dashboard/4_7/html/dash_conditions_alerts.html)
* [Using the Avere Control Panel Support Tab](https://azure.github.io/Avere/legacy/ops_guide/4_7/html/support_overview.html#general-information-upload)
* [Configuring Cluster Support](https://azure.github.io/Avere/legacy/ops_guide/4_7/html/gui_support.html)
* [Avere vFXT for Azure Documentation](https://docs.microsoft.com/azure/avere-vfxt/)
* [Prepare to create the Avere vFXT](https://docs.microsoft.com/azure/avere-vfxt/avere-vfxt-prereqs)
* [Avere vFXT for Azure FAQ](https://docs.microsoft.com/azure/avere-vfxt/avere-vfxt-faq)
* [Avere Legacy Documentation](https://azure.github.io/Avere/)
* [Avere Configuration Guide](https://azure.github.io/Avere/legacy/ops_guide/4_7/html/ops_conf_index.html)
* [Avere Dashboard Guide](https://azure.github.io/Avere/legacy/dashboard/4_7/html/ops_dashboard_index.html)
