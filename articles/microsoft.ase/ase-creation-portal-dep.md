<properties
	pageTitle="Creation  Issues\Portal Deployment"
	description="Creation  Issues\Portal Deployment"
	service="microsoft.ase"
	resource="ase"
	authors="cts-shrahman,shrahman"
    ms.author="shrahman, curibe"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32608429"
	resourceTags=""
	productPesIds="16533"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="2aca238a-96c5-4d78-bec2-6e193757c4b4"
	ownershipId="Compute_AppService"
/>

# Creation Issues\Portal Deployment


## **Recommended Steps**

If the ASE deployment was triggered more than 12 hours ago and it failed, the ASE will be deleted and VNet Verifier will not be able to find it. If it is within 12 hours, please use VNet Verifier to verify whether the NSGs and UDRs attached to the ASE's subnet are correctly configured.
<br>

Most of issues related to ASE creation are due to ASE dependencies being blocked by customer's NSGs, UDRs, Firewalls and other routes.
<br> 

Please follow the next recommendations to avoid the deployment failure: <br>

- For a new ASE deployment, start with a default "clean" networking setup if possible to ensure the deployment itself completes
Once the ASE has been successfully created, you can configure the NSG and Route Tables properly with your requirements (Contemplating the Networking Considerations for an App Service Environment)
- The ASE subnet has to be dedicated, meaning nothing else can be in the subnet but the ASE
- We recommend a size of /24 with 256 addresses. Be sure to choose an address space that allows for future growth as you cannot change this setting later.
- If you create the Subnet in conjunction with the ASE creation process, this might avoid most of the creation issues caused by customer's NSGs and UDRs
- If you already have the Subnet created, try disassociating any NSG on the target subnet and create a default route table with one entry for 0.0.0.0/0 with next hop for internet
- If you are advertising BGP routes on the VNet (for ExpressRoute) you should also disable the Virtual network gateway route propagation from the "Configuration" blade in the Route Table
<br>

## **Recommended Documents**

* [ASE Dependencies](https://docs.microsoft.com/azure/app-service/environment/network-info#ase-dependencies) <br>
* [NSGs](https://docs.microsoft.com/azure/app-service/environment/network-info#network-security-groups) <br>
* [Routes](https://docs.microsoft.com/azure/app-service/environment/network-info#routes)<br>
* [Configure your App Service Environment with forced tunneling](https://docs.microsoft.com/azure/app-service/environment/forced-tunnel-support)<br>
* [Networking considerations for an App Service Environment](https://docs.microsoft.com/azure/app-service/environment/network-info)
* [Locking down an ASE](https://docs.microsoft.com/azure/app-service/environment/firewall-integration)

