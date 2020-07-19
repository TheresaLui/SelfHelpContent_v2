<properties
pageTitle="The Application Gateway basic listener has higher priority rule than multisite listener."
description="The Application Gateway basic listener has higher priority rule than multisite listener."
infoBubbleText="Issues with your Application Gateway were detected. See details on the right."
service="microsoft.network"
resource="ApplicationGateway"
authors="chadmath"
ms.author="chadmat"
displayOrder="10"
articleId="AppGwBasicListenerPriority"
diagnosticScenario="AppGwBasicListenerPriority"
selfHelpType="Diagnostics"
supportTopicIds="32436961,32573483,32582834,32436964,32436960,32582828,32582829,32582830,32582825,32582826,32582827,32582831,32582832,32436961,32573483,32582834,32436962,32565734,32565735,32565736,32582833"
resourceTags="windows"
productPesIds="15922"
cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="CloudNet_AzureApplicationGateway"
/>
# Microsoft Azure has identified an issue with your Application Gateway listeners

<!--issueDescription-->
We have identified that your Application Gateway **'<!--$Gatewayname-->[GatewayName]<!--/$Gatewayname-->'** has a basic listener, **'<!--$basiclistener-->[ListenerName]<!--/$basiclistener-->'**, with a higher priority than a multi-site listener for the same port with a rule **'<!--$rulename-->[RuleName]<!--/$rulename-->'** associated. Configure your multi-site listeners first prior to configuring a basic listener. This will ensure that traffic gets routed to the correct backend. If a basic listener is listed first and matches an incoming request, it will be processed by that listener.
<!--/issueDescription-->

## **Recommended Steps**

1. Review and note the settings for your basic listener named '<!--$basiclistener-->[ListenerName]<!--/$basiclistener-->'
2. Delete basic listener named '<!--$basiclistener-->[ListenerName]<!--/$basiclistener-->'
3. Create a new basic listener using the noted settings from step 1 above
