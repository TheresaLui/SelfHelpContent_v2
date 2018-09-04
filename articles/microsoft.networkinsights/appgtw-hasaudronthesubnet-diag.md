<properties
pageTitle="Application Gateway has a UDR on the subnet"
description="Application Gateway has a UDR on the subnet"
infoBubbleText="Issues with your Application Gateway were detected. See details on the right."
service="microsoft.network"
resource="ApplicationGateway"
authors="Parag"
displayOrder="10"
articleId="ApplicationGatewayhasaUDRonthesubnet"
diagnosticScenario="ApplicationGatewayhasaUDRonthesubnet"
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public"
/>
# Application Gateway Diagnostic Result
<!--issueDescription-->
Microsoft Azure has identified Application Gateway: **<!--$GateWayName-->[GatewayName]<!--/$GatewayName-->** in Subnet: **<!--$SubnetName-->[SubnetName]<!--/$SubnetName-->** has the following UDR associated: **<!--$UDRName-->[UDRName]<!--$UDRName-->**.
<!--/issueDescription-->
## **Steps to resolve the issue**
Remove the UDR from the Application Gateway subnet.