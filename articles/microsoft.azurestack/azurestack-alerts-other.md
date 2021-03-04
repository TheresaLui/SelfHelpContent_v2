<properties
  pagetitle="Azure Stack Hub Alerts"
  service="microsoft.azurestack"
  resource="registrations"
  ms.author="justinha,patricka"
  selfhelptype="Generic"
  supporttopicids="32629237,32737192,32737318,32741954,32745918"
  resourcetags=""
  productpesids="16226,17058,17131,17057,17322"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="azurestack-alerts-other"
  ownershipid="StorageMediaEdge_AzureStack_Hub" />
# Azure Stack Hub Alerts

Resolve most Azure Stack Hub alerts with the following sections.

**Common Issues**

* Error: "The Azure Stack Usage Bridge service is unable to connect to the remote service"
  Make sure that required URLs and ports are enabled. For more information, see [Ports and protocols (inbound)](https://docs.microsoft.com/azure-stack/operator/azure-stack-integrate-endpoints#ports-and-protocols-inbound). 

* False-positive alert in the Administrator portal for an **Invalid Time Source** after applying the 2002 update.
 This alert can be ignored and will be fixed in an upcoming release. For more information, see [Azure Stack Hub known issues](https://docs.microsoft.com/azure-stack/operator/known-issues?view=azs-2002).  

* Usage Bridge alert "AADSTS900439: Confidential Client requests are not supported" or "certificateValidationError"
  The simplest solution is to [re-register Azure Stack Hub](https://docs.microsoft.com/azure-stack/operator/azure-stack-registration). Make sure you are using correct [endpoints](https://docs.microsoft.com/azure-stack/operator/azure-stack-integrate-endpoints) to register.  

**NOTE**: Before you create a support ticket, review [**Release notes**](https://docs.microsoft.com/azure-stack/operator/release-notes) and [**Known issues**](https://docs.microsoft.com/azure-stack/operator/known-issues) for the update you are applying (choose from the Version drop-down menu). This may save you time and effort.


## **Recommended Steps**

A critical alert should be addressed urgently because it can impact users. Always attempt the remediation steps in the alert before opening a support case. In some alerts, you can select **Repair** in the Remediation details of the alert to resolve the issue. You can run **Repair** again if it fails. 

## **Recommended Documents**

* [Monitor health and alerts in Azure Stack Hub](https://docs.microsoft.com/azure-stack/operator/azure-stack-monitor-health?view=azs-2002)
* [Validate Azure Stack Hub system state](https://docs.microsoft.com/azure-stack/operator/azure-stack-diagnostic-test)
