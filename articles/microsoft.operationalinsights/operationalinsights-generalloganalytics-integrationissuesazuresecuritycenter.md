
<properties
pageTitle="Integration issues: Azure Security Center"
description="Integration issues: Azure Security Center"
service="microsoft.operationalinsights"
symptomID=""
infoBubbleText=""
resource="operationalinsightsaccounts"
authors="Yanivsh"
selfHelpType="generic"
supportTopicIds="32612471"
resourceTags=""
productPesIds="15725"
cloudEnvironments="Public, Fairfax"
articleId = "operationalinsights-generalloganalytics-integrationissuesazuresecuritycenter"
/>

# Integration issues: Azure Security Center

To Check if security solution installed on the relevant workspace by following this steps : 
 
* Open log analytics
* Press on the relevant workspace
* Under the general menu press on the solutions section  
* New blade will be open with list of solutions 
* Look for : Security or SecurityCenterFree names.

If it doesn’t appear in this list please follow this article to add it via azure security center pricing tier option.
https://docs.microsoft.com/en-us/azure/security-center/security-center-enable-data-collection#using-an-existing-workspace

**Important:** Your Billing will be define based on the type of the security solution that installed on your worksopace.

## **Recommended documents**
* Security Center Pricing Tier https://azure.microsoft.com/en-us/pricing/details/security-center/
* Data collection in Azure Security Center https://docs.microsoft.com/en-us/azure/security-center/security-center-enable-data-collection
* Azure Security Center frequently asked questions (FAQ) https://docs.microsoft.com/en-us/azure/security-center/security-center-faq
