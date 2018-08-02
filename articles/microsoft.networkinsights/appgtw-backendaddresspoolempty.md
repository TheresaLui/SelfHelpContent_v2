<properties
pageTitle="The Application Gateway backend address pool is empty."
description="The Application Gateway backend address pool is empty."
infoBubbleText="Issues with your Application Gateway were detected. See details on the right."
service="microsoft.network"
resource="ApplicationGateway"
authors="chadmath"
displayOrder="10"
articleId="AppGwBackendAddressPoolEmpty"
diagnosticScenario="AppGwBackendAddressPoolEmpty"
selfHelpType="Diagnostics"
supportTopicIds="32436961,32573483,32582834"
resourceTags="windows"
productPesIds="15922"
cloudEnvironments="Public"
/>
# Microsoft Azure has identified an issue with your Application Gateway backend pool
<!--issueDescription-->
We have identified that your Application Gateway, **'<!--$Gatewayname-->[GatewayName]<!--/$Gatewayname-->'**, has a backend address pool, '**<!--$BackendPool-->[BackendAddressPoolName]<!--/$BackendPool-->'**, that is empty. The resources in your Application Gateway's backend address pool are the resources hosting your web solutions. With an empty backend address pool there are no resources to respond to the Application Gateway's health probes and no way to serve your solution to your end users. You can check the health of your backend pools using the 'Backend Health' blade for your Application Gateway. Here, you will receive the status of your backend pools and detailed descriptions, if health issues are detected, and what you can do to resolve.
<!--/issueDescription-->
## **Steps to resolve**
1. Find your Application Gateway: '<!--$Gatewayname-->[GatewayName]<!--/$Gatewayname-->' in the [Azure portal](http://portal.azure.com).
2. Select the 'Backend Pools' blade
3. Select the backend pool: '<!--$BackendPool-->[BackendAddressPoolName]<!--/$BackendPool-->'
4. Select the drop down and select IP Address or FDQN, Virtual Machine, or VMSS
5. Complete the remaining fields and Save.

You can also follow the [visual guide for creating backend servers](https://docs.microsoft.com/azure/application-gateway/application-gateway-create-gateway-portal#create-backend-servers).
