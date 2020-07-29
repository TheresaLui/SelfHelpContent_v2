<properties
  pagetitle="Configure Multi-site Hosting"
  service="microsoft.network"
  resource="applicationgateways"
  ms.author="surmb"
  selfhelptype="Generic"
  supporttopicids="32582827"
  resourcetags=""
  productpesids="15922"
  cloudenvironments="public,fairfax,blackforest,mooncake,usnat,ussec"
  articleid="3209a960-3d4f-4220-8eb1-a99848e6a5cc"
  ownershipid="CloudNet_AzureApplicationGateway" />

# Configure Multi-site Hosting

Application Gateway allows you to configure routing based on host name or domain name for more than one web application on the same gateway. It allows you to configure a more efficient topology for your deployments by adding up to 100+ websites to one application gateway. Each website can be directed to its own backend pool.

For example, three domains, contoso.com, fabrikam.com, and adatum.com, point to the IP address of the application gateway. You'd create three multi-site listeners and configure each listener for the respective port and protocol setting. You can also define wildcard host names in a multi-site listener and up to 5 host names per listener. To learn more, see [wildcard host names in listener (preview).](https://docs.microsoft.com/azure/application-gateway/multiple-site-overview#wildcard-host-names-in-listener-preview)

## **Recommended Documents**

* Configure multi-site hosting for an Application Gateway using [Azure Portal](https://docs.microsoft.com/azure/application-gateway/create-multiple-sites-portal) or [Azure PowerShell](https://docs.microsoft.com/azure/application-gateway/tutorial-multiple-sites-powershell) or [Azure CLI](https://docs.microsoft.com/azure/application-gateway/tutorial-multiple-sites-cli)
* [Multiple site hosting](https://docs.microsoft.com/azure/application-gateway/multiple-site-overview) overview on Application Gateway
* [Wildcard host names and up to 5 host names per listener - preview](https://docs.microsoft.com/azure/application-gateway/multiple-site-overview#wildcard-host-names-in-listener-preview)