<properties
    pageTitle="Autoscale action failed"
    description="Troubleshooting failed autoscale actions"
    service="microsoft.insights"
    resource="components"
    authors="vgorbenko"
    ms.author="vitalyg"
    displayOrder="2"
    articleId="autoscale-action-failed"
    selfHelpType="generic"
    supportTopicIds="32683735"
    productPesIds="15527"
    cloudEnvironments="public,fairfax,mooncake,blackforest,usnat, ussec"
	ownershipId="AzureMonitoring_Essentials"
/>

# <-- autoscale-action-failed -->

There are several reasons why Azure autoscale action may be failing. You can use **Activity Log** to verify results of autoscale actions and review errors.

## **Recommended Steps**

1. Confirm that the scale actions are failing. Open **Activity Logs** and apply filter to the subscription your autoscale setting is in. Then choose **Autoscale** as the event category, and review the failure messages.
1. Match the failure message with the cause of problem and follow the recommended action outlined below:

**If the Autoscale setting is for a Virtual Machine Scale Set (VMSS):**

| Error | Reason |
|-------|--------|
|"Resource is disabled and therefore marked as read only" | Please check the Azure Policy set on your VMSS. If there is a read-only Policy, Autoscale service will not be able to scale your resource. Note that it may take several minutes for the autoscale to pick up recent changes to the policy.|
|"Operation results in exceeding quota limits of Core. Maximum allowed: *value*", "Operation results in exceeding quota limits of standardNVPromoFamily Cores. Maximum allowed: *value*" or "Operation results in exceeding quota limits of standardDv2Family Core" | You have reached the quota limits for the number of CPU cores. Review the default quota and request an increase as outlined in [Standard quota: Increase limits by VM series](https://docs.microsoft.com/azure/azure-supportability/per-vm-quota-requests#request-a-standard-quota-increase-from-the-help--support-pane).|
|"VMSS updates are not allowed while there is a Rolling Upgrade in progress" | This message indicates that the VMSS is updating, which is an expected state of scale action. Autoscale will continue to monitor the status and will try to trigger the action again when updates are completed, if the scale action conditions still match.|

**If the Autoscale setting is for Cloud Services:**

| Error | Reason |
|-------|--------|
|"Operation threw an exception: The remote server returned an unexpected response: (409) Conflict." | Please file a support request against the Autoscale service. Include the error message along with resource name and resource group of the target resource.|
|"Operation threw an exception: The remote server returned an unexpected response: (400) Bad Request." | Please file a support request against the Autoscale service. Include the error message along with resource name and resource group of the target resource.|

**If the Autoscale setting is for App service server farms:**

| Error | Reason |
|-------|--------|
|"Storage usage quota exceeded. Cannot update or delete a server farm. Please make sure your file system storage is below the limit of the target pricing tier." | This message indicates that autoscale is hitting the App services quotas. Please review the [per-SKU disk storage quotas](https://azure.microsoft.com/pricing/details/app-service/plans/). Remove the unused files and website content to lower your aggregate disk usage so that it stays within the "Disk Space" limits or switch to a service plan with higher limits.|
|"Multiple workers are not allowed for *(resource name)* serverfarm with In-App MySql site *(site name)*." | The In-App MySql feature is only supported on single instance app service plans.  Learn about the In-App MySql feature and limitations at [Announcing MySQL in-app for Web Apps](https://azure.github.io/AppService/2016/08/18/Announcing-MySQL-in-app-for-Web-Apps-%28Windows%29.html).|

## **Recommended Documents**

* [Overview of autoscale in Microsoft Azure Virtual Machines, Cloud Services, and Web Apps](https://docs.microsoft.com/azure/azure-monitor/platform/autoscale-overview)
* [Get started with autoscale in Azure](https://docs.microsoft.com/azure/azure-monitor/platform/autoscale-get-started)
* [Best practices for Azure Monitor autoscale](https://docs.microsoft.com/azure/azure-monitor/platform/autoscale-best-practices)
* [Troubleshooting guide for Azure Monitor autoscale](https://docs.microsoft.com/azure/azure-monitor/platform/autoscale-troubleshoot)
