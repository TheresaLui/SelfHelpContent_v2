<properties
pageTitle="Application Gateway Has No Http Listeners with LB Rules"
description="Application Gateway Has No Http Listeners with LB Rules"
infoBubbleText="Issues with your Application Gateway were detected. See details on the right."
service="microsoft.network"
resource="Application Gateway"
authors="Paragpk89"
ms.author="paragk"
displayOrder="10"
articleId="AppGwNoHttpListenerWithLoadBalancingRulesInsight"
diagnosticScenario="AppGwNoHttpListenerWithLoadBalancingRulesInsight"
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public,Fairfax,Mooncake, usnat, ussec"
ownershipId="CloudNet_AzureApplicationGateway"
/>

# Application Gateway Missing HTTP Listener
<!--issueDescription-->
We have found that your Application Gateway **'<!--$Gatewayname-->[GatewayName]<!--/$Gatewayname-->'** has no HttpListeners with LoadBalancingRules associated. The Application Gateway will not function until at least one HttpListener has LoadBalancingRules associated.
<!--/issueDescription-->

## **Recommended Steps**

1. Open the [Azure portal](https://portal.azure.com)
2. Browse to your Application Gateway **'<!--$Gatewayname-->[GatewayName]<!--/$Gatewayname-->'**
3. Click on the "Listeners" blade
4. Select the Listener you wish to use or create one if you do not have one listed
5. Associate a LoadBalancingRule with the Listener from step #4

## **Recommended Documents**

* [Azure CLI Reference - HTTP Listeners](https://docs.microsoft.com/cli/azure/network/application-gateway/http-listener?view=azure-cli-latest)
* [Load Balancing Rules](https://docs.microsoft.com/rest/api/load-balancer/loadbalancerloadbalancingrules/get)
