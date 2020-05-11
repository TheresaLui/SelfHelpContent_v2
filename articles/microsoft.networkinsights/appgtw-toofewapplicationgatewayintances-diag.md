<properties
pageTitle="Application Gateway has too few instances"
description="Application Gateway has too few instances"
infoBubbleText="Issues with your Application Gateway were detected. See details on the right."
service="microsoft.network"
resource="ApplicationGateway"
authors="chadmath"
displayOrder="10"
articleId="ApplicationGatewayhastoofewinstances"
diagnosticScenario="ApplicationGatewayhastoofewinstances"
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec"
	ownershipId="CloudNet_AzureApplicationGateway"
/>
# Application Gateway Performance Affected by Too Few Instances Running
<!--issueDescription-->
We found **<!--$InstanceCount-->[InstanceCount]<!--/$InstanceCount-->** Application Gateway instances running. Application Gateway supports high availability scenarios when you have two or more instances deployed. Azure distributes these instances across update and fault domains to ensure that all instances will not fail at the same time.
<!--/issueDescription-->
## **Steps to resolve the issue**
Add at least one additional Application Gateway instance in the 'Configuration' blade of your Application Gateway.
