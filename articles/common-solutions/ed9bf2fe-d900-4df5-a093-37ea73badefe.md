<properties
  pagetitle="Private Link and Service Endpoint"
  service="microsoft.web"
  resource="sites"
  ms.author="shrahman"
  selfhelptype="Generic"
  supporttopicids="32784809"
  productpesids="16170"
  cloudenvironments="public, fairfax, mooncake, blackforest, ussec, usnat"
  disableclouds=""
  articleid="ed9bf2fe-d900-4df5-a093-37ea73badefe"
  ownershipid="Compute_AppService" />
# Private Link and Service Endpoint

Refer to the following limitaions when setting up private links and Service Endpoints for App Service.

## **Recommended Steps**

### Setting up private links for App Service:
* Private endpoint can only be accessed from the VNET(and the connected network) in which the private endpoint is created.
* App Service will no longer be available over its public endpoint. Trying to access App Service over its public endpoint will result in an "HTTP 403" message.
* Check the DNS resolution from the client which is accessing the App Service private endpoint. It should resolve to the private IP assigned from the private endpoint. Only then will the app be accessible.
* Remote debugging is currently not available with Private Endpoints.
* Private Endpoints is not available for slots.

### Setting up Service Endpoints for App Service:
* If remote debugging is performed from an Azure Virtual Machine, disable **Microsoft.Web** service endpoint on the subnet corresponding to that Virtual Machine.


## **Recommended Documents**

* [Using Private Endpoints for Azure Web App](https://docs.microsoft.com/azure/app-service/networking/private-endpoint)
* [Tutorial: Connect to a web app using an Azure Private Endpoint](https://docs.microsoft.com/azure/private-link/tutorial-private-endpoint-webapp-portal)
* [Service Endpoints](https://docs.microsoft.com/azure/virtual-network/virtual-network-service-endpoints-overview)
