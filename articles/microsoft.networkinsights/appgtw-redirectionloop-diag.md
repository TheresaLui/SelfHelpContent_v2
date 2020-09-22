<properties
pageTitle="Application Gateway has a Redirection Loop"
description="Application Gateway has a Redirection Loop"
infoBubbleText="Issues with your Application Gateway were detected. See details on the right."
service="microsoft.network"
resource="ApplicationGateway"
authors="chadmath"
displayOrder="1"
articleId="AppGwRedirectionLoopInsight"
diagnosticScenario="AppGwRedirectionLoopInsight"
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec"
	ownershipId="CloudNet_AzureApplicationGateway"
/>
# Application Gateway Redirection Loop Detected
<!--issueDescription-->
We have identified that your Application Gateway, **'<!--$Gatewayname-->[GatewayName]<!--/$Gatewayname-->'**, has a loop in redirection. Redirection setting **'<!--$RedirectionSetting-->[RedirectionSetting]<!--/$RedirectionSetting-->'** has a target listener, **<!--$TargetListener-->[TargetListener]<!--/$TargetListener-->**, which has protocol of **<!--$Protocol-->[Protocol]<!--/$Protocol-->**, site of **<!--$Site-->[Site]<!--/$Site-->** and port of **<!--$Port-->[Port]<!--/$Port-->**. The redirected url **'<!--$Url-->[Url]<!--/$Url-->'** has already been visited. This effectively 'black holes' your network traffic breaking your solution.
<!--/issueDescription-->
## **Steps to resolve the issue**
Review your listener and redirection configuration ensuring that your redirect listeners and target listeners are not redirecting to previous URLs or listeners in the redirection chain. 
