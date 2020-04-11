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
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="ce07d030-1bb9-4b90-a426-1e486ec7fd28"
	ownershipId="Compute_AppService"
/>
# Questions on creating and managing ASE
## **Recommended documents**
**ASE Creation:**<br>
[Most frequent issues when deploying (creating) a new Azure App Service Environment (ASE).](https://blogs.msdn.microsoft.com/waws/2016/05/13/most-frequent-issues-when-deploying-creating-a-new-azure-app-service-environment-ase/)<br>
[How to create an App Service Environment V2 (ASEv2)?](https://azure.microsoft.com/blog/announcing-app-service-environment-v2/)<br>
[How to create an Internal Load Balancing (ILB) ASE?](https://docs.microsoft.com/azure/app-service-web/app-service-environment-with-internal-load-balancer)<br>
**ASE Configuration and Management:**<br>
[How to scale a Web App in an App Service Environment(ASE)?](https://docs.microsoft.com/azure/app-service-web/app-service-web-scale-a-web-app-in-an-app-service-environment)<br> 
[How to auto-scale Web Apps in an App Service Environment( ASE)?](https://docs.microsoft.com/azure/app-service/app-service-environment-auto-scale)<br>
**ASE is unavailable or unhealthy:**<br>
An App Service Environment(ASE) will be marked as Unhealthy if any of its dependencies (inbound or outbound), are being blocked by either a bad NSG, a bad UDR or Force Tunneling being enabled. 
For more information,  please review [Networking considerations for an App Service environment](https://docs.microsoft.com/azure/app-service/app-service-environment/network-info) and 
[Network Configuration Details for App Service Environments with ExpressRoute](https://docs.microsoft.com/azure/app-service-web/app-service-app-service-environment-network-configuration-expressroute)<br>