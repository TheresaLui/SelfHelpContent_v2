<properties
  pagetitle="ASE Down\Multiple Web Apps Affected"
  service="microsoft.web"
  resource="hostingenvironments"
  ms.author="shrahman"
  selfhelptype="Generic"
  supporttopicids="32608428"
  resourcetags=""
  productpesids="16533"
  cloudenvironments="public,fairfax,usnat,ussec,blackforest,mooncake"
  articleid="c3206276-847f-493c-a54e-629cbc1b583c"
  ownershipid="Compute_AppService" />
# ASE Down\Multiple Web Apps Affected

Most customers resolve their App Service Environment (ASE) issues with the following resources.

## **Recommended steps**
When multiple web apps are not functioning as expected on an ASE, the ASE should be inspected to make sure it is heathy. The most common cause of an unhealthy ASE is a misconfigured ASE network. This could be from a misconstructed route table or network security group or block dependencies at a firewall that are necessary for the correct functioning of an ILB ASE.

  References:
  * [Networking considerations for an App Service Environment](https://docs.microsoft.com/azure/app-service/environment/network-info)
  * [Locking down an App Service Environment (Firewall Dependencies)](https://docs.microsoft.com/azure/app-service/environment/firewall-integration#dependencies)
  * [Configure your App Service Environment with forced tunneling](https://docs.microsoft.com/azure/app-service/environment/forced-tunnel-support#change-the-egress-endpoint-for-your-ase)
  * [ASE v3 networking](https://docs.microsoft.com/azure/app-service/environment/networking)

Your ASE may be healthy but ALL the applications in the ASE are showing the same 5xx errors. This state can be caused by front-end servers in the ASE being unable to keep up with the load and reporting high CPU usage. Find the front-end CPU percentage in the **Overview** blade for your ASE. If you see greater than 80% CPU usage, add an additional front-end server by changing your **Front End Scale Ratio**.

  Reference:
  * [Use an App Service Environment (Frontend Scaling)](https://docs.microsoft.com/azure/app-service/environment/using-an-ase#front-end-scaling)
