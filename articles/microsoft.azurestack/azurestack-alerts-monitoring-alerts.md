<properties
    pageTitle="Azure Stack alerts"
    description="General guidance for Azure Stack alert issues"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629171,32630574"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public"
	articleId="84de2e54-0b99-46e4-afb8-1ecf4e31679f"
/>

# Azure Stack alerts

Azure Stack includes infrastructure monitoring capabilities that enable you to view health and alerts for an Azure Stack region. The **Region Management** tile, pinned by default in the administrator portal for the Default Provider Subscription, lists all the deployed regions of Azure Stack. The tile shows the number of active critical and warning alerts for each region and is your entry point into the health and alert functionality of Azure Stack.

## **Recommended Steps**

1. To view the health state in the portal, click the region that you want to view in the Region management tile
2. View the health state of infrastructure roles and of resource providers by following steps to [view and manage component health state](https://docs.microsoft.com/azure/azure-stack/azure-stack-monitor-health#view-and-manage-component-health-state)
3. [View active alerts](https://docs.microsoft.com/azure/azure-stack/azure-stack-monitor-health#view-alerts) for each Azure Stack region is available directly from the Region management blade
4. You can also integrate an [external monitoring solutions with Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-integrate-monitor)

## **Recommended Documents**

* [Monitor health and alerts in Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-monitor-health)
* [Integrate external monitoring solution with Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-integrate-monitor)
