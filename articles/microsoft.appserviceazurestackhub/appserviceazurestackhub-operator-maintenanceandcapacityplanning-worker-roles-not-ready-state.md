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

### 1. Verify worker roles are in a "ready" state 

There can be multiple causes preventing a worker role from reaching the "ready" state, which will prevent deployment of applications. 

#### File server health check failure

If you've deployed to an existing virtual network and are using an internal IP address to connect to your file server, you must add a network security group (NSG) rule to allow traffic between the worker role subnet and your file server. If you didn't, the file server health check will fail on the worker role.

Check the worker role logs to verify file server health check completion:

1. Sign in to the Azure Stack Hub administrator portal.
2. Go to the "App Service" service, select the "Roles" blade.
3. Verify whether any of the Web Worker roles have not reached a "Ready" status.
4. For any worker roles not in a "Ready" status, select the role.
5. On the work role "Instances" blade, select the role instance that has not reached a "Ready" status.
6. On the worker role "Instance" blade, select the "Logs" button.
7. On the "Server Logs" blade, scan the log messages. Look for warning message "Failed exercise FileServer at MM/DD/YYYY HH:MM:SS".
8. If you find the above message, go to the "Network Security Group" blade, and select the "WorkersNsg" security group.
9. Verify that the [post-deployment steps for NSG configuration](https://docs.microsoft.com/azure-stack/operator/azure-stack-app-service-deploy?pivots=state-connected#post-deployment-steps) have been completed. These steps will walk you through configuration of an outbound security rule, to enable SMB traffic between the worker subnet and the file server.

#### Incorrect server password configuration

If a password was specified incorrectly during install, you will need to proceed with opening a support case to get it resolved. 

### 2. Verify adequate resource capacity (TBD)

Scale up/out: [Add workers and infrastructure in Azure App Service on Azure Stack Hub](https://docs.microsoft.com/azure-stack/operator/azure-stack-app-service-add-worker-roles) ??

## **Recommended Documents**

* [App Service overview](https://docs.microsoft.com/azure-stack/operator/azure-stack-app-service-overview)
