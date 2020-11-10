<properties
    pageTitle="MSEE Provider Address-To-Customer Address (PA-to-CA) Mapping Not Found"
    description="MSEE Provider Address-To-Customer Address (PA-to-CA) Mapping Not Found"
    infoBubbleText="MSEE Provider Address-To-Customer Address (PA-to-CA) Mapping Not Found.  See details on right."
    service="microsoft.network"
    resource="ExpressRoute"
    authors="jaredro"
    ms.author="jaredr80"
    displayOrder=""
    articleId="ExRRnmBrooklynConsistencyMseeCaPaMappingNotFoundInsight"
    diagnosticScenario="ExRRnmBrooklynConsistencyMseeCaPaMappingNotFoundInsight"
    selfHelpType="diagnostics"
    supportTopicIds="32586802, 32586803, 32586804, 32586805, 32539949, 32539950, 32539954, 32539963"
    resourceTags="windows"
    productPesIds="15480"
    cloudEnvironments="public, Fairfax, usnat, ussec"
 	ownershipId="CloudNet_AzureExpressRoute"
/>
# MSEE Provider Address-To-Customer Address (PA-to-CA) Mapping Not Found

ExpressRoute uses mappings from RNM (Regional Network Manager) for PA-to-CA translation. The mappings are not found in GWM, and need to be refreshed and set.

'**<!--$Message-->[Message]<!--/$Message-->**' <br>
VNetID: '**<!--$VNetID-->[VNetID]<!--/$VNetID-->**'  <br>

## **Recommended Steps**
* Execute **Jarvis Actions** operation: **Brooklyn->ExR Diagnostic Operations->Fix Vnet Config in Goalstate** for VNetId: '**<!--$VNetID-->[VNetID]<!--/$VNetID-->**'
