
<properties
pageTitle="Problems creating workspace"
description="Problems creating workspace"
service="microsoft.operationalinsights"
resource="workspaces"
symptomID=""
infoBubbleText=""
authors="yossiy"
authorAlias="yossiy"
displayorder="11"
selfHelpType="resource"
supportTopicIds="32612513"
resourceTags=""
productPesIds="15725"
cloudEnvironments="Public, Fairfax"
/>

# Problems While Creating Workspace
Review common problems related to workspace creation:

## **Recommended Steps**

* Error message: *Pricing tier doesn't match the subscription's billing model.*<br>

This error can occur in these cases:<br>

   * Create a workspace with *'pergb2018'* pricing plan (introduced in April 2018), while the subscription is not in *'pergb2018'* pricing plan.
   * Create a *'Free'* workspace in subscription in *'pergb2018'* pricing plan.<br>

    Workspaces in subscriptions that were created, or [changed](https://docs.microsoft.com/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#moving-to-the-new-pricing-model) to *'pergb2018'* can only be in the *'pergb2018'* pricing plan. When creating a workspace with *'PerNode'* or *'Standalone'* pricing plan in *'pergb2018'* pricing plan subscription, the workspace pricing plan is set to *'pergb2018'* instead.

* [Can’t create workspaces in West Central US region](https://docs.microsoft.com/azure/log-analytics/log-analytics-faq#q-why-i-cant-create-workspaces-in-west-central-us-region)<br>
This region is at temporary capacity limit. The limit is planned to be addressed in the first half of 2019.

* Don't have sufficient permissions<br>
You need to be assigned with *'Log Analytics Contributor'* permissions for workspace creation.<br>

## **Recommended Documents**
* [New pricing model and Operations Management Suite subscription entitlements](https://docs.microsoft.com/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model-and-operations-management-suite-subscription-entitlements)
* [Moving to the new pricing model](https://docs.microsoft.com/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#moving-to-the-new-pricing-model)
* [Managing access to Log Analytics using Azure permissions](https://docs.microsoft.com/azure/log-analytics/log-analytics-manage-access?toc=/azure/azure-monitor/toc.json#managing-access-to-log-analytics-using-azure-permissions)
