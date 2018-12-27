<properties
pageTitle="Integration issues: Azure Security Center"
description="Integration issues: Azure Security Center"
service="microsoft.operationalinsights"
symptomID=""
infoBubbleText=""
resource="operationalinsightsaccounts"
authors="Yanivsh"
authoralias = "yanivsh@microsoft.com"
selfHelpType="generic"
supportTopicIds="32612471"
productPesIds="15725"
cloudEnvironments="Public, Fairfax"
articleId = "operationalinsights-generalloganalytics-integrationissuesazuresecuritycenter"
/>

# Integration issues: Azure Security Center
Security Center collects data from your Azure virtual machines (VMs) and non-Azure computers . Data is collected using the Microsoft Monitoring Agent and copies the data to your workspace for analysis.

## **Recommended steps**
 To Check if security solution installed on the relevant workspace by following this steps:<br>
 
* Open log analytics
* Press on the relevant workspace
* Under the general menu press on the solutions section  
* New blade will be open with list of solutions 
* Look for : Security or SecurityCenterFree names.<br>

If it doesn’t appear in this list please follow this article to add it via azure security center pricing tier option.
(https://docs.microsoft.com/azure/security-center/security-center-enable-data-collection#using-an-existing-workspace)

**Important:**<br>
Your billing will be define based on the type of the security solution that installed on your worksopace.<br>

## **Recommended documents**
* [Security Center Pricing Tier](https://azure.microsoft.com/pricing/details/security-center/)
* [Data collection in Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-enable-data-collection)
* [Azure Security Center frequently asked questions (FAQ)](https://docs.microsoft.com/azure/security-center/security-center-faq)