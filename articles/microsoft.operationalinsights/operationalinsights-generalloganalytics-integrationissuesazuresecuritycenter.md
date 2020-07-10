<properties
pageTitle="Integration issues: Azure Security Center"
description="Integration issues: Azure Security Center"
service="microsoft.operationalinsights"
symptomID=""
infoBubbleText=""
resource="operationalinsightsaccounts"
authors="Yanivsh"
ms.author="fifa1111"
selfHelpType="generic"
supportTopicIds="32612471"
productPesIds="15725"
cloudEnvironments="Public, Fairfax, usnat, ussec"
articleId="4d77366c-4655-4c8b-86e4-f599e9e00b47"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# Integration issues: Azure Security Center
Security Center collects data from your Azure virtual machines (VMs) and non-Azure computers. Data is collected using the Microsoft Monitoring Agent and copies the data to your workspace for analysis.

## **Recommended Steps**

Check if Security Center is installed on the VM:

1. Open log analytics
2. Click on the relevant workspace
3. Under the general menu, click on solutions
4. In the new blade with the list of solutions, look for "Security" or "Security Center Free"

If Security Center does not appear in your solutions, please review the [Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-enable-data-collection#using-an-existing-workspace) offerings.

## **Recommended Documents**

* [Security Center Pricing Tier](https://azure.microsoft.com/pricing/details/security-center/)
* [Data collection in Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-enable-data-collection)
* [Azure Security Center frequently asked questions (FAQ)](https://docs.microsoft.com/azure/security-center/security-center-faq)
