<properties
  pagetitle="ASE down or marked as unhealthy or suspended"
  service="microsoft.web"
  resource="hostingenvironments"
  ms.author="shrahman"
  selfhelptype="Generic"
  supporttopicids="32608420"
  resourcetags=""
  productpesids="16533"
  cloudenvironments="public,fairfax,usnat,ussec,blackforest,mooncake"
  articleid="cec8676f-8b41-43ac-8608-752f9480cf5b"
  ownershipid="Compute_AppService" />
# ASE down or marked as unhealthy or suspended

##  **Recommended Steps**

If the Azure Platform cannot connect to the app service environment (ASE) management IP's on port 454-455, the ASE is marked as unhealthy. 

**ASE Unhealthy** has different behaviors. There may be a banner that says the ASE is unhealthy. ASE blades may not load or may show a rainy cloud icon. Other signs of an unhealthy ASE are: you can't upload ILB Cert, create a new web app in the ASE, or scale workers or front ends.

The ASE is suspended if it's unhealthy for 7 consecutive days. A suspended ASE will have the content preserved, but the ASE itself will be removed. You can **resume** the ASE from a resource explorer provided the underlying problem causing the ASE to be unhealthy has been resolved (DNS, VNET, NSG, UDR, Firewall). If the ASE is unhealthy for 100 days, it will be deleted.

The most common cause of an unhealthy ASE is a misconfigured ASE network. This can result from a misconstructed route table or network security group, or from block dependencies at a firewall that are necessary for the correct functioning of an ILB ASE.

References:
   * [Networking considerations for an App Service Environment](https://docs.microsoft.com/azure/app-service/environment/network-info)
  * [Locking down an App Service Environment (Firewall Dependencies)](https://docs.microsoft.com/azure/app-service/environment/firewall-integration#dependencies)
  * [Configure your App Service Environment with forced tunneling](https://docs.microsoft.com/azure/app-service/environment/forced-tunnel-support#change-the-egress-endpoint-for-your-ase)
  * [ASE v3 networking](https://docs.microsoft.com/azure/app-service/environment/networking)
	 
Your ASE may be healthy but ALL the applications in the ASE are showing the same 5xx errors. This state can be caused by the Frontend servers in the ASE consuming high cpu and not able to keep up with the load. The Frontend CPU percentage can be found in the overview blade for your ASE. If you are seeing high cpu, over 80%, please add an additional Frontend server by changing your Front End Scale Ratio.

Reference:
  * [Use an App Service Environment (Frontend Scaling)](https://docs.microsoft.com/azure/app-service/environment/using-an-ase#front-end-scaling)
