<properties
    pageTitle="Validation State Does Not Match"
    description="Validation State Does Not Match"
    infoBubbleText="Validation State Does Not Match.  See details on right."
    service="microsoft.network"
    resource="ExpressRoute"
    authors="jaredro"
    ms.author="jaredr80"
    displayOrder=""
    articleId="ExRMseeCircuitConfigValidationStateDoesNotMatchInsight"
    diagnosticScenario="ExRMseeCircuitConfigValidationStateDoesNotMatchInsight"
    selfHelpType="diagnostics"
    supportTopicIds="32586802, 32586803, 32586804, 32586805, 32539949, 32539950, 32539954, 32539963"
    resourceTags="windows"
    productPesIds="15480"
    cloudEnvironments="public, Fairfax, usnat, ussec"
 	ownershipId="CloudNet_AzureExpressRoute"
/>

# Validation State Does Not Match
<!--/issueDescription-->
The current state of the circuit's config in GWM does not match the device config, which may be causing inconsistencies with the customer's experience.

*Private and Microsoft peering do not apply to this insight.*

* '**<!--$Message-->[Message]<!--/$Message-->**' <br>
* ServiceKey: '**<!--$ServiceKey-->[ServiceKey]<!--/$ServiceKey-->**'  <br>
* MSEE: '**<!--$MSEE-->[MSEE]<!--/$MSEE-->**' <br>
* VRF Name: '**<!--$VRF-->[VRF]<!--/$VRF-->**' <br>
<!--/issueDescription-->

## **Recommended Steps**

* Execute **Jarvis Actions** operation: **Brooklyn->ExR Service Operations->Force Apply Device Configuration** for ServiceKey: '**<!--$ServiceKey-->[ServiceKey]<!--/$ServiceKey-->**'
