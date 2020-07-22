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

There can be multiple causes for a worker role to not show in a "ready" state.

### File server health check failure

Check logs to verify whether the file server health check failed:
1. Sign in to the Azure Stack Hub administrator portal.
2. Go to the "App Service" service, select the "Roles" blade.
3. Verify whether any of the Web Worker roles have not reached a "Ready" status.
4. For any worker roles not in a "Ready" status, select the role.
5. On the work role "Instances" blade, select the role instance that has not reached a "Ready" status.
6. On the worker role "Instance" blade, select the "Logs" button.
7. On the "Server Logs" blade, scan the log messages. Look for "Failed to exercise FileServer message (after 3 tries)"
8. If you find the above message, got to the "Network Security Group" blade, and select the "WorkersNsg" security group.
9. TBD... 

### Missing network security group configuration

If you're deploying to an existing virtual network and using an internal IP address to connect to your file server, you must [add an outbound network security group rule](https://docs.microsoft.com/azure-stack/operator/azure-stack-app-service-deploy?pivots=state-connected#post-deployment-steps).             

### Incorrect server password configuration

If a password was specified incorrectly during install, you will need to proceed with opening a support case to get it resolved. 

### TBD

TBD: [Add workers and infrastructure in Azure App Service on Azure Stack Hub](https://docs.microsoft.com/azure-stack/operator/azure-stack-app-service-add-worker-roles) ??

## **Recommended Documents**

* [App Service overview](https://docs.microsoft.com/azure-stack/operator/azure-stack-app-service-overview)
