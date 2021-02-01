<properties
    pageTitle="Azure Virtual Network - Cannot delete VNet because of Azure App Service integration"
    description="Azure Virtual Network - Cannot delete VNet because of Azure App Service integration"
    service="microsoft.network"
    resource="virtualnetwork"
    authors="v-miegge"
    ms.author="Mario.Liu"
    selfHelpType="generic"
    supportTopicIds="32781376"
    resourceTags=""
    productPesIds="15526"
    ownershipId="CloudNet_VirtualNetwork"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="3546f045-d7f5-4033-bf43-92080ea407c8"
/>

# Azure Virtual Network - Cannot delete VNet because of Azure App Service integration

If you integrated your application with an Azure Virtual Network (VNet) first, be sure to disconnect your application from the VNet before you delete your application. If you delete the application first, you may not be able to delete this virtual network, as the service association link on the subnet of this VNet still exists. You can fix the issue by following these steps:

## **Recommended Steps**

1. Create App Service Plan with the same name as the deleted one
2. Create App Service with the same name as the deleted one
3. Link the App Service with the VNET subnet
4. Disconnect VNet from **App Service** > **Networking** > **VNet integration** > **Disconnect**
5. Delete the subnet
6. Delete the virtual network
7. Delete the App Service and the App Service Plan

## **Recommended Documents**

- [Manage VNet Integration](https://docs.microsoft.com/azure/app-service/web-sites-integrate-with-vnet#manage-vnet-integration)
