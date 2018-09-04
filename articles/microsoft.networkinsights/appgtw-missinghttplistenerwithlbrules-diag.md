<properties
pageTitle="My Application Gateway is missing a Http listener with load balancing rules."
description="My Application Gateway is missing a Http listener with load balancing rules."
service="microsoft.network"
resource="ApplicationGateway"
authors="chadmath"
displayOrder="10"
articleId="AppGwNoHttpListenerWithLoadBalancingRulesInsight"
diagnosticScenario="AppGwNoHttpListenerWithLoadBalancingRulesInsight"
selfHelpType="Diagnostics"
supportTopicIds="32436961,32573483,32582834,32436964,32436960,32582828,32582829,32582830,32582825,32582826,32582827,32582831,32582832,32436961,32573483,32582834,32436962,32565734,32565735,32565736,32582833"
resourceTags="windows"
productPesIds="15922"
cloudEnvironments="Public"
/>
# Microsoft Azure has identified that your Application Gateway is missing a 'Http Listener' with load balancing rules
<!--issueDescription-->
We have identified your Application Gateway: **<!--$Gatewayname-->[GatewayName]<!--/$Gatewayname-->** has no Http Listeners with Load Balancing Rules associated. The Application Gateway will not function until at least one Http Listener has Load Balancing Rules associated.
<!--/issueDescription--> 
## **Steps to resolve**

1. Go to the [Azure Portal](https://portal.azure.com)
2. Find your Application Gateway, **<!--$Gatewayname-->[GatewayName]<!--/$Gatewayname-->**
3. Go to the 'Listeners' blade to identify the desired listener. (Create one if one does not exist)
4. Go to the 'Rules' blade and create a rule that references the listener from step #3
