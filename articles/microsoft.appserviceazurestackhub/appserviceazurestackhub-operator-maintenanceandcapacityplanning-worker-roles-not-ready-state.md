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

There can be multiple reasons a worker role is unable to reach a "ready" state, which will prevent deployment of applications. 

### Missing network security group (NSG) role

If you've deployed to an existing virtual network and are using an internal IP address to connect to your file server, you must add an NSG rule to allow traffic between the worker role subnet and your file server. If you don't, the file server health check will fail on the worker role.

Check the worker role logs to verify file server health check completion:

1. Sign in to the Azure Stack Hub administrator portal.
2. Go to the "App Service" service, select the "Roles" blade.
3. Verify whether any of the Web Worker roles have not reached a "Ready" status.
4. For any worker roles not in a "Ready" status, select the role.
5. On the worker role "Instances" blade, select the role instance that has not reached a "Ready" status.
6. On the worker role "Instance" blade, select the "Logs" button.
7. On the "Server Logs" blade, filter on the warning level and scan the log messages. Look for warning message "Failed exercise FileServer at MM/DD/YYYY HH:MM:SS".
8. If you find the above message, go to the "Network Security Group" blade, and select the "WorkersNsg" security group.
9. Verify that the [post-deployment steps for NSG configuration](https://docs.microsoft.com/azure-stack/operator/azure-stack-app-service-deploy?pivots=state-connected#post-deployment-steps) have been completed. These steps will walk you through configuration of an outbound security rule, to enable SMB traffic between the worker subnet and the file server.

### Incorrect Windows Server image 

For deployment in a disconnected environment, you must use a Windows Server image that has .NET 3.5.1 SP1 activated. See [Download items from the Azure Marketplace](https://docs.microsoft.com/azure-stack/operator/azure-stack-app-service-before-you-get-started?pivots=state-disconnected) for details.

### Other causes

For all other causes, proceed with opening a support case to contact a support engineer for resolution.

## **Recommended Documents**

* [App Service overview](https://docs.microsoft.com/azure-stack/operator/azure-stack-app-service-overview)
