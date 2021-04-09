<properties
  pagetitle="Scale ASE Instances&#xD;"
  service="microsoft.web"
  resource="hostingenvironments"
  ms.author="shrahman"
  selfhelptype="Generic"
  supporttopicids="32608417"
  resourcetags=""
  productpesids="16533"
  cloudenvironments="public,fairfax,usnat,ussec,blackforest,mooncake"
  articleid="f00eb4b5-9dde-4bd0-a322-b85485666c49"
  ownershipid="Compute_AppService" />
# Scale ASE Instances

## **Recommended Steps**

If scaling an ASE App Service Plan is taking too long, this is because although scaling an App Service plan on an ASE includes the automatic addition ofinfrastructure, there's a delay while the infrastructure is being deployed. ASE scaling operations depend on multiple internal components, such as VM scale sets and RDFE, and will take at least 20-30 minutes.

You can use autoscaling for an App Service Plan hosted on an ASE, but we recommend using schedule-based autoscaling rather than metric-based autoscaling. If the ASE scales based on metrics, the scaling operation might complete too late to impact the metric, and your users' experiences may be impacted. A better approach is to anticipate the time when user load will be higher and create autoscale rules for those schedules.

For more information, see:
 * [How scaling works for an ASE](https://docs.microsoft.com/azure/app-service/environment/using#how-scale-works)
 * [Best practices for Autoscale](https://docs.microsoft.com/azure/azure-monitor/autoscale/autoscale-best-practices)

Because scaling operations deploy ASE resources, they're subject to the same ASE networking considerations as the initial ASE deployment. If the ASE is unhealthy, no scaling operations can take place.  

For information on how to configure an ILB ASE V2 network and its dependencies, see:
  * [Networking considerations for an App Service Environment](https://docs.microsoft.com/azure/app-service/environment/network-info)
  * [Locking down an App Service Environment (Firewall Dependencies)](https://docs.microsoft.com/azure/app-service/environment/firewall-integration#dependencies)
  * [Configure your App Service Environment with forced tunneling](https://docs.microsoft.com/azure/app-service/environment/forced-tunnel-support#change-the-egress-endpoint-for-your-ase)
