<properties
pageTitle="My Application Gateway has a multi-site listener with a default health probe."
description="My Application Gateway has a multi-site listener with a default health probe."
infoBubbleText="Issues with your Application Gateway were detected. See details on the right."
service="microsoft.network"
resource="ApplicationGateway"
authors="chadmath"
ms.author="chadmat"
displayOrder="10"
articleId="AppGwMultiSiteListenerWithDefaultProbe"
diagnosticScenario="AppGwMultiSiteListenerWithDefaultProbe"
selfHelpType="Diagnostics"
supportTopicIds="32436961,32573483,32582834,32436964,32436960,32582828,32582829,32582830,32582825,32582826,32582827,32582831,32582832,32436961,32573483,32582834,32436962,32565734,32565735,32565736,32582833"
resourceTags="windows"
productPesIds="15922"
cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="CloudNet_AzureApplicationGateway"
/>

# Microsoft Azure has identified an issue with your Application Gateway's multi-site listener
<!--issueDescription-->
We have identified that your Application Gateway: **<!--$Gatewayname-->[GatewayName]<!--/$Gatewayname-->** has a multi-site listener **<!--$ListenerName-->[ListenerName]<!--/$ListenerName-->** that is configured with the default probe configured in the Backend Http Settings **<!--$BackendHttpSettingName-->[BackendHttpSettingsName]<!--/$BackendHttpSettingName-->**. Using host headers with default probes can cause backend health probe disruptions. See below to resolve.
<!--/issueDescription-->

## **Recommended Steps**

* If the backend server requires a host header, you should [configure a custom probe](https://docs.microsoft.com/azure/application-gateway/application-gateway-create-probe-portal)
