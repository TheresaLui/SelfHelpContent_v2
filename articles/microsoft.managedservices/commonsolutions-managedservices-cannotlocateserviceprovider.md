<properties
	pageTitle="Cannot locate service provider IDs"
	description="Cannot locate service provider IDs"
	infoBubbleText="Cannot locate service provider IDs"
	service="microsoft.managedservices"
	resource="managedservices"
	authors="prukulka"
	ms.author="prukulka"
	displayOrder=""
	articleId="CommonSolutions-managedservices-cannotlocateserviceprovider"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32642164"
	resourceTags=""
	productPesIds="16761"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Compute_AzureLighthouse"
/>

# Cannot locate service provider IDs

Most users are able to locate service provider IDs using the steps below.

## **Recommended Steps**

### **Can't find subscription or Tenant ID values?**

- **Azure portal**
Your tenant ID can be seen by hovering over your account name on the upper right-hand side of the Azure portal, or by selecting Switch directory. To select and copy your tenant ID, search for "Azure Active Directory" from within the portal, then select Properties and copy the value shown in the Directory ID field. To find the ID of a subscription in the customer tenant, search for "Subscriptions" and then select the appropriate subscription ID.

- **PowerShell**
Log in first with Connect-AzAccount if you're not using Cloud Shell : `Select-AzSubscription <subscriptionId>`

- **Azure CLI**
Log in first with az login if you're not using Cloud Shell: `az account set --subscription <subscriptionId/name>` `az account show`
    
## **Recommended Documents**

* [How to onboard customer & gather-tenant-and-subscription-details](https://docs.microsoft.com/azure/lighthouse/how-to/onboard-customer#gather-tenant-and-subscription-details)



