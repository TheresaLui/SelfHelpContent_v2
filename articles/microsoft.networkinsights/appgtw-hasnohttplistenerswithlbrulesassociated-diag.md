<properties
pageTitle="Application Gateway Has No Http Listeners with LB Rules"
description="Application Gateway Has No Http Listeners with LB Rules"
infoBubbleText="Issues with your Application Gateway were detected. See details on the right."
service="microsoft.network"
resource="Application Gateway"
authors="Parag"
displayOrder="10"
articleId="appgtwhasnohttplistenerswithlbrulesassociated"
diagnosticScenario="appgtwhasnohttplistenerswithlbrulesassociated"
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public"
/>
# Application Gateway Missing Http Listener 
<!--issueDescription-->
We have found that your Application Gateway **'<!--$Gatewayname-->[GatewayName]<!--/$Gatewayname-->'** has no HttpListeners with LoadBalancingRules associated. The Application Gateway will not function until at least one HttpListener has LoadBalancingRules associated.
<!--/issueDescription-->
## **Steps to resolve this issue**
Please complete the configuration by associating LoadBalancingRules with at least one HttpListener in the [Azure portal](https://portal.azure.com).