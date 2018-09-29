<properties
pageTitle="Application Gateway Has No Http Listeners with LB Rules"
description="Application Gateway Has No Http Listeners with LB Rules"
infoBubbleText="Issues with your Application Gateway were detected. See details on the right."
service="microsoft.network"
resource="Application Gateway"
authors="Parag"
displayOrder="10"
articleId="AppGwNoHttpListenerWithLoadBalancingRulesInsight"
diagnosticScenario="AppGwNoHttpListenerWithLoadBalancingRulesInsight"
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

1. Open the [Azure portal](https://portal.azure.com)
2. Browse to your Application Gateway **'<!--$Gatewayname-->[GatewayName]<!--/$Gatewayname-->'**
3. Select the 'Listeners' blade
4. Selet the Listener you wish to use or create one if you do not have one listed
5. Associate associate a LoadBalancingRule with the Listener from step #4
