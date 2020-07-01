<properties
	pageTitle="Configuring and Managing Function Apps/Deployment Slots"
	description="Configuring and Managing Function Apps/Deployment Slots"
	service="microsoft.web"
	resource="functions"
	authors="cts-shrahman,cts-shrahman"
    ms.author="shrahman,danzha"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32630465"
	resourceTags=""
	productPesIds="16072"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="7e610ca6-fcf9-4243-b96e-7d22abb5823b"
	ownershipId="Compute_AppService"
/>

# Configuring and Managing Function Apps/Deployment Slots

## **Recommended Steps**

Azure App Service provides a Deployment Slots feature, which allows users to validate app changes in a staging deployment slot before swapping it with the production slot and easily roll back. Azure Function Apps use the Azure App Service infrastructure, and provides the same feature. Deployment Slots is still in Preview and is on the way to general availability for Function Apps. <br>

### **Known Limitations**<br>

1. [Consumption plan](https://docs.microsoft.com/azure/azure-functions/functions-scale#consumption-plan) supports adding **one** deployment slot. If you require additional slots, please host function app on a [dedicated plan](https://docs.microsoft.com/azure/azure-functions/functions-scale#consumption-plan). 
2. Please manage slot in Function App blade instead of going to Function App -> All settings, since "Deployment Slots" and "Deployment Slots(Preview)" are greyed out there 
3. The warning message that appears when you create a deployment slot in Azure Portal, *"You can’t use the deployment slot after Jan 2019. You need to move “Deployment Slot(Preview) experience. Please click here and try new experience”*, is for Azure App Service Deployment Slots. Customers are still able to use existing Function App slots experience even after Jan 2019.

## **Recommended Documents**

* [Deployments Slots Previews for Azure Functions](https://blogs.msdn.microsoft.com/appserviceteam/2017/06/13/deployment-slots-preview-for-azure-functions/) 
* [Internals of Swap with Preview](https://blogs.msdn.microsoft.com/waws/2016/12/12/slot-swap-with-preview/)

