<properties
  pagetitle="Portal Issues&#xD;"
  service="microsoft.web"
  resource="hostingenvironments"
  ms.author="shrahman"
  selfhelptype="Generic"
  supporttopicids="32608415"
  resourcetags=""
  productpesids="16533"
  cloudenvironments="public,fairfax,usnat,ussec,blackforest,mooncake"
  articleid="9cd832b5-11a2-406d-a200-c6ea37444cfb"
  ownershipid="Compute_AppService" />
# Portal Issues

## **Recommended Steps**
* The portal has additional dependencies required for portal access that are not needed for running App Services hosted on an ASE. These additional dependencies may not be included in your networking configuration. Please see [Portal dependencies](https://docs.microsoft.com/azure/app-service/environment/network-info#portal-dependencies) for more information.

* Both Functions and WebJobs are supported on an ILB ASE but for the portal to work with them, you must have network access to the SCM site. This means your browser must either be on a host that is either in or connected to the virtual network. 

* If your ILB ASE has a domain name that does not end in *appserviceenvironment.net*, you will need to get your browser to trust the HTTPS certificate being used by your scm site.
