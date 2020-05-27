<properties
pageTitle="My Application Gateway has a missing frontend port."
description="My Application Gateway has a missing frontend port."
infoBubbleText="Issues with your Application Gateway were detected. See details on the right."
service="microsoft.network"
resource="ApplicationGateway"
authors="chadmath"
ms.author="chadmat"
displayOrder="10"
articleId="AppGwNoFrontendPortFoundInsight"
diagnosticScenario="AppGwNoFrontendPortFoundInsight"
selfHelpType="Diagnostics"
supportTopicIds="32436961,32573483,32582834,32436964,32436960,32582828,32582829,32582830,32582825,32582826,32582827,32582831,32582832,32436961,32573483,32582834,32436962,32565734,32565735,32565736,32582833"
resourceTags="windows"
productPesIds="15922"
cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="CloudNet_AzureApplicationGateway"
/>

# Microsoft Azure has identified that your Application Gateway is missing a frontend port

<!--issueDescription-->
We have identified that your Application Gateway: **<!--$Gatewayname-->[GatewayName]<!--/$Gatewayname-->** has no Frontend Port configured.
<!--/issueDescription-->

## **Recommended Steps**

1. Go to the [Azure Portal](https://portal.azure.com)
2. Find your Application Gateway, **<!--$Gatewayname-->[GatewayName]<!--/$Gatewayname-->**
3. Select the 'Frontend IP configurations' blade and configure a Frontend Port
4. Select the 'Listeners' blade. Use the Frontend Port created in step 3 in the Http Listener
