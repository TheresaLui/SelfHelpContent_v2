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
cloudEnvironments="Public"
/>
# Application Gateway Performance Affected by Too Few Instances Running
<!--issueDescription-->
Found **<!--$InstanceCount-->[InstanceCount]<!--/$InstanceCount-->** application gateway instances running. The suggested number is at least 2 for load balancing and fault tolerance. Application Gateway supports high availability scenarios when you have two or more instances deployed. Azure distributes these instances across update and fault domains to ensure that all instances do not fail at the same time. Application Gateway supports scalability by adding multiple instances of the same gateway to share the load. 
<!--/issueDescription-->
## **Steps to resolve the issue**
Add at least one additional Application Gateway instance in the 'Configuration' blade of your Application Gateway.