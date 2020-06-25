<properties
pageTitle="Application Gateway No Rule Found For Http Listener"
description="Application Gateway No Rule Found For Http Listener"
infoBubbleText="Issues with your Application Gateway were detected. See details on the right."
service="microsoft.network"
resource="ApplicationGateway"
authors="chadmath"
displayOrder="10"
articleId="AppGwNoRuleFoundForHttpListenerInsight"
diagnosticScenario="AppGwNoRuleFoundForHttpListenerInsight"
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec"
	ownershipId="CloudNet_AzureApplicationGateway"
/>
# Application Gateway Listener Missing Load-Balancing Rules
<!--issueDescription-->
We have identified that your Application Gateway **<!--$GatewayName-->[GatewayName]<!--/$GatewayName-->** has a Http listner named **'<!--$ListenerName-->[ListenerName]<!--/$ListenerName-->'** that has no load balancing rules associated. This HttpListener will not function until LoadBalancingRules are associated.
<!--/issueDescription-->
## **Steps to resolve the issue**
To resolve the issue please associate load balancing rules with the HttpListener **'<!--$ListenerName-->[ListenerName]<!--/$ListenerName-->'** in the 'Rules' blade of your Application Gateway **<!--$GatewayName-->[GatewayName]<!--/$GatewayName-->**.