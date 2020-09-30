<properties
    pageTitle="App Service operator maintenance and capacity planning capacity management scale out issues"
    description="App Service operator maintenance and capacity planning capacity management scale out issues"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT, v-miegge"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32742844"
    resourceTags=""
    productPesIds="17136"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="appserviceazurestackhub-operator-maintenanceandcapacityplanning-capacity-management-scale-out-issues"
	ownershipId="StorageMediaEdge_AzureStack_Hub"
/>

# App Service operator maintenance and capacity planning capacity management scale out issues


## **Recommended Steps**

To scale out Management, Front End, or Publisher roles, follow the same steps selecting the appropriate role type. Controllers aren't deployed as Scale Sets and therefore two should be deployed at installation time for all production deployments.

* [Add workers and infrastructure in Azure App Service on Azure Stack Hub](https://docs.microsoft.com/azure-stack/operator/azure-stack-app-service-add-worker-roles)

## **Recommended Documents**

* [App Service overview](https://docs.microsoft.com/azure-stack/operator/azure-stack-app-service-overview)
