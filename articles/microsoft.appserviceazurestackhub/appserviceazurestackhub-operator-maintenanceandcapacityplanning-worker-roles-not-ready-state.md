<properties
    pageTitle="App Service operator maintenance and capacity planning worker roles not ready state"
    description="App Service operator maintenance and capacity planning worker roles not ready state"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32742881"
    resourceTags=""
    productPesIds="17136"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="appserviceazurestackhub-operator-maintenanceandcapacityplanning-worker-roles-not-ready-state"
	ownershipId="StorageMediaEdge_AzureStack_Hub"
/>

# App Service operator maintenance and capacity planning worker roles not ready state


## **Recommended Steps**

There can be multiple reasons your worker roles are not showing a "ready" state.

### File server health check failure

Check logs to verify whether the file server health check failed:
- App Service - Roles blade
- Choose broken roles, go into logs
- Look for "Failed to exercise FileServer message (after 3 tries)"
- Go to worker NSG blade 

### Network Security Group configuration

If you're deploying to an existing virtual network and using an internal IP address to connect to your file server, you must [add an outbound network security group rule](https://docs.microsoft.com/azure-stack/operator/azure-stack-app-service-deploy?pivots=state-connected#post-deployment-steps).             

### Server password configuration

If a password was specified incorrectly during during install, you will need to go ahead and open a support case to get it resolved. 

### TBD

TBD: [Add workers and infrastructure in Azure App Service on Azure Stack Hub](https://docs.microsoft.com/azure-stack/operator/azure-stack-app-service-add-worker-roles) ??

## **Recommended Documents**

* [App Service overview](https://docs.microsoft.com/azure-stack/operator/azure-stack-app-service-overview)
