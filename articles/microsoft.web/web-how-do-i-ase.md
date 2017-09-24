<properties
	pageTitle="Questions on Backup and Restore"
	description="Questions on backup and restore"
	service="microsoft.web"
	resource="sites"
	authors="sudhat"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32589275"
	resourceTags=""
	productPesIds="14748"
	cloudEnvironments="public"
/>
# Questions on creating and managing ASE
## **Recommended documents**
**ASE Creation:**
[Most frequent issues when deploying (creating) a new Azure App Service Environment (ASE).](https://blogs.msdn.microsoft.com/waws/2016/05/13/most-frequent-issues-when-deploying-creating-a-new-azure-app-service-environment-ase/)
[How to create an App Service Environment V2 (ASEv2)?](https://azure.microsoft.com/blog/announcing-app-service-environment-v2/)[How to create an Internal Load Balancing (ILB) ASE?](https://docs.microsoft.com/azure/app-service-web/app-service-environment-with-internal-load-balancer)
**ASE Configuration and Management:**
[How to scale a Web App in an App Service Environment(ASE)?](https://docs.microsoft.com/azure/app-service-web/app-service-web-scale-a-web-app-in-an-app-service-environment)  
[How to auto-scale Web Apps in an App Service Environment( ASE)?](https://docs.microsoft.com/azure/app-service/app-service-environment-auto-scale) 
**ASE is unavailable or unhealthy:**
An App Service Environment(ASE) will be marked as Unhealthy if any of its dependencies (inbound or outbound), are being blocked by either a bad NSG or a bad UDR or Force Tunneling being enabled. For more information:  
[Networking considerations for an App Service environment](https://docs.microsoft.com/azure/app-service/app-service-environment/network-info)
[Network Configuration Details for App Service Environments with ExpressRoute](https://docs.microsoft.com/azure/app-service-web/app-service-app-service-environment-network-configuration-expressroute)