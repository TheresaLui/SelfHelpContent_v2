<properties
  pagetitle="Creation Issues\Portal Deployment&#xD;"
  service="microsoft.web"
  resource="hostingenvironments"
  ms.author="curibe,shrahman"
  selfhelptype="Generic"
  supporttopicids="32608429"
  resourcetags=""
  productpesids="16533"
  cloudenvironments="public,fairfax,usnat,ussec,blackforest,mooncake"
  articleid="2aca238a-96c5-4d78-bec2-6e193757c4b4"
  ownershipid="Compute_AppService" />
# Creation Issues\Portal Deployment


## **Recommended Steps**

If you triggered an ASE deployment that failed more than 12 hours ago, the ASE will be deleted and VNet Verifier won't be able to find it. If the ASE deployment was triggered within 12 hours, use VNet Verifier to verify whether the NSGs and UDRs attached to the ASE's subnet are correctly configured.
<br>

Most ASE creation issues result from ASE dependencies being blocked by NSGs, UDRs, Firewalls, and other routes.
<br> 

To avoid deployment failures, follow the next recommendations: <br>

- For a new ASE deployment, start with the default networking setup if possible to ensure that the deployment can successfully complete 
After the ASE has been successfully created, configure the NSG and Route Tables properly with your requirements. See [Networking considerations for an App Service Environment](https://docs.microsoft.com/azure/app-service/environment/network-info).
- The ASE subnet must be dedicated. This means, nothing but the ASE can be in the subnet.
- We recommend a size of /24 with 256 addresses. Make sure to choose an address space that allows for future growth as you cannot change this setting later.
- If you create the subnet in conjunction with the ASE creation process, this can avoid most creation issues caused by customer's NSGs and UDRs
- If you already created the subnet, disassociate any NSGs on the target subnet, and create a default route table with one entry for 0.0.0.0/0 with next hop for internet
- If you are advertising BGP routes on the VNet (for ExpressRoute), disable the Virtual network gateway route propagation from the **Configuration** blade in the Route Table
<br>

## **Recommended Documents**

* [ASE Dependencies](https://docs.microsoft.com/azure/app-service/environment/network-info#ase-dependencies) <br>
* [NSGs](https://docs.microsoft.com/azure/app-service/environment/network-info#network-security-groups) <br>
* [Routes](https://docs.microsoft.com/azure/app-service/environment/network-info#routes)<br>
* [Configure your App Service Environment with forced tunneling](https://docs.microsoft.com/azure/app-service/environment/forced-tunnel-support)<br>
* [Locking down an ASE](https://docs.microsoft.com/azure/app-service/environment/firewall-integration)
