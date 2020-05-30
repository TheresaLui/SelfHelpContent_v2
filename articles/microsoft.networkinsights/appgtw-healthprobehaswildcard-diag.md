<properties
pageTitle="My Application Gateway health probe path has a wildcard."
description="My Application Gateway health probe path has a wildcard."
infoBubbleText="Issues with your Application Gateway were detected. See details on the right."
service="microsoft.network"
resource="ApplicationGateway"
ms.author="chadmat"
authors="chadmath"
displayOrder="10"
articleId="AppGwHealthProbeHasWildCard"
diagnosticScenario="AppGwHealthProbeHasWildCard"
selfHelpType="Diagnostics"
supportTopicIds="32436961,32573483,32582834,32436964,32436960,32582828,32582829,32582830,32582825,32582826,32582827,32582831,32582832,32436961,32573483,32582834,32436962,32565734,32565735,32565736,32582833"
resourceTags="windows"
productPesIds="15922"
cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="CloudNet_AzureApplicationGateway"
/>

# Microsoft Azure has identified that your Application Gateway has a health probe path with a wildcard

<!--issueDescription-->
We have identified that your Application Gateway: **<!--$Gatewayname-->[GatewayName]<!--/$Gatewayname-->** has a health probe **<!--$ProbeName-->[ProbeName]<!--/$ProbeName-->** that has a wildcard in the path **<!--$Path-->[Path]<!--/$Path-->**. Probe path should be a specific path on the backend server.
<!--/issueDescription-->

## **Recommended Steps**

1. Go to the [Azure Portal](https://portal.azure.com)
2. Find your Application Gateway, **<!--$Gatewayname-->[GatewayName]<!--/$Gatewayname-->**
3. Select the 'Health Probes' blade
4. Select the health probe **<!--$ProbeName-->[ProbeName]<!--/$ProbeName-->**
5. Include a specific path value
