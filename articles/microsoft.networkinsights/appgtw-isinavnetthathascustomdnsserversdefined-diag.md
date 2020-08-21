<properties
pageTitle="Application Gateway is in a VNet that has custom DNS servers defined"
description="Application Gateway is in a VNet that has custom DNS servers defined"
infoBubbleText="Issues with your Application Gateway were detected. See details on the right."
service="microsoft.network"
resource="ApplicationGateway"
ms.author="chadmat"
authors="chadmath"
displayOrder="10"
articleId="AppGwInVnetWithCustomDns"
diagnosticScenario="AppGwInVnetWithCustomDns"
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec"
	ownershipId="CloudNet_AzureApplicationGateway"
/>

# Microsoft Azure has identified custom DNS for your Vnet containing your Application Gateway

<!--issueDescription-->
We have identified that your Application Gateway: **<!--$GatewayName-->[GatewayName]<!--/$GatewayName-->** in VNet: **<!--$VnetName-->[VnetName]<!--/$VnetName-->** has custom DNS servers defined. Your Application Gateway may not be able to resolve the names of your backend pool resources.
<!--/issueDescription-->

## **Recommended Steps**

1. Go to the [Azure Portal](https://portal.azure.com)
2. Find your Application Gateway: **<!--$GatewayName-->[GatewayName]<!--/$GatewayName-->**
3. Open the 'Backend Pools' blade, then click on the backend pool and make note of the IP address or URL
4. Next, navigate to VNet **<!--$VnetName-->[VnetName]<!--/$VnetName-->** in the portal
5. Open the 'DNS Servers' blade and make note of the IPs
6. Log into the DNS servers and ping the fully qualified domain name (FQDN) of each of your backend servers identified in step #3 above
7. Ensure the custom DNS servers are able to resolve all names in the backend address pool
