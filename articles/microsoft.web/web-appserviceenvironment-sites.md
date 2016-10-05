<properties
	pageTitle="app service environment"
	description="app service environment"
	service="microsoft.web"
	resource="sites"
	authors="aashu"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32542253"
	resourceTags=""
	productPesIds="14748"
	cloudEnvironments="public"
/>

# app service environment
## **Recommended steps**
<b>In an App Service Environment (ASE) why can I only create one App Service Plan (ASP) even though I have 2 workers available?</b><br>
In order to provide fault tolerance, an App Service Environment (ASE) requires that for each worker pool you have at least one additional compute resource allocated.<br>
Please review the following article for more information:
[Configuring ASE - Fault-tolerance considerations](https://azure.microsoft.com/documentation/articles/app-service-web-configure-an-app-service-environment/)

<b>ASE creation timing out</b><br>
Sometimes creating an App Service Environment (ASE) will fail with the following error in the Activity logs:<br>
 
    ResourceID: /subscriptions/{SubscriptionID}/resourceGroups/Default-Networking/providers/Microsoft.Web/hostingEnvironments/{ASEname}
    Error:{"error":{"code":"ResourceDeploymentFailure","message":"The resource provision operation did not complete within the allowed timeout period."}}


Make sure that NONE of the following are true:<br>
    1. Subnet is too small <br>
    2. Subnet is not empty <br>
    3. ExpressRoute not allowing network connectivity requirements of an ASE <br>
    4. Bad Network Security Group (NSG) not allowing network connectivity requirements of an ASE <br>
    5. Forced Tunneling enabled <br>

For more information, please review: <br>
[How to Create an App Service Environment](https://azure.microsoft.com/documentation/articles/app-service-web-how-to-create-an-app-service-environment/#Overview) <br>
[Most frequent issues when deploying (creating) a new Azure App Service Environment (ASE)](https://blogs.msdn.microsoft.com/waws/2016/05/13/most-frequent-issues-when-deploying-creating-a-new-azure-app-service-environment-ase/)

## **Recommended documents**
[What is an App Service Environment?](https://azure.microsoft.com/documentation/articles/app-service-app-service-environment-intro/)<br>
[Creating an App Service Environment](https://azure.microsoft.com/documentation/articles/app-service-web-how-to-create-an-app-service-environment/)<br>
[Creating Apps in an App Service Environment](https://azure.microsoft.com/documentation/articles/app-service-web-how-to-create-a-web-app-in-an-ase/)<br>
[Configuring an App Service Environment](https://azure.microsoft.com/documentation/articles/app-service-web-configure-an-app-service-environment/)<br>
[Scaling Apps in an App Service Environment](https://azure.microsoft.com/documentation/articles/app-service-web-scale-a-web-app-in-an-app-service-environment/)<br>
[Network Security and Architecture](https://azure.microsoft.com/documentation/articles/app-service-app-service-environment-network-architecture-overview/)<br>
[Setting Up a Geo-Distributed App Footprint](https://azure.microsoft.com/documentation/articles/app-service-app-service-environment-geo-distributed-scale/)<br>
[Implementing a Layered Security Architecture](https://azure.microsoft.com/documentation/articles/app-service-app-service-environment-layered-security/)<br>
[Configuring a Web Application Firewall with an App Service Environment](https://azure.microsoft.com/documentation/articles/app-service-app-service-environment-web-application-firewall/)<br>
[Using Auto-Scale with an App Service Environment](https://azure.microsoft.com/documentation/articles/app-service-environment-auto-scale/)<br>
[Securing Inbound Traffic](https://azure.microsoft.com/documentation/articles/app-service-app-service-environment-control-inbound-traffic/)<br>
[Connecting to Backend Resources](https://azure.microsoft.com/documentation/articles/app-service-app-service-environment-securely-connecting-to-backend-resources/)<br>
[ExpressRoute and App Service Environments](https://azure.microsoft.com/documentation/articles/app-service-app-service-environment-network-configuration-expressroute/)<br>
[Custom Configuration Settings for App Service Environments](https://azure.microsoft.com/documentation/articles/app-service-app-service-environment-custom-settings/)
