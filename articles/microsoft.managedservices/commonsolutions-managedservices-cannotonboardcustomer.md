<properties
	pageTitle="Cannot onboard customer"
	description="Cannot onboard customer"
	infoBubbleText="Cannot onboard customer"
	service="microsoft.managedservices"
	resource="managedservices"
	authors="prukulka"
	ms.author="prukulka"
	displayOrder=""
	articleId="CommonSolutions-managedservices-cannotonboardcustomer-cantfindIDs"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32642166"
	resourceTags=""
	productPesIds="16761"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Compute_AzureLighthouse"
/>

# Cannot onboard customer

Most users are able to resolve their customer onboarding to Lighthouse issue using the steps below.

## **Recommended Steps**

**Can't deploy template successfully?**

- To onboard your customer, you'll need to create an [Azure Resource Manager](https://docs.microsoft.com/azure/azure-resource-manager/index) template for your offer with the following information. The mspOfferName and mspOfferDescription values will be visible to the customer when viewing offer details in the [Service providers page](https://docs.microsoft.com/azure/lighthouse/how-to/view-manage-service-providers) of the Azure portal.
- The onboarding process requires an Azure Resource Manager template (provided in our [samples repo](https://github.com/Azure/Azure-Lighthouse-samples/) and a corresponding parameters file that you modify to match your configuration and define your authorizations

**Can't deploy template at resource group level?**

- Deployments must be performed at the subscription level by a non-guest account in the customer's tenant who has the Owner built-in role for the subscription being onboarded (or which contains the resource groups that are being onboarded). This deployment can't be initiated in the Azure portal, but can be done by using PowerShell or Azure CLI, as shown in [Deploy the Azure Resource Manager templates](https://docs.microsoft.com/azure/lighthouse/how-to/onboard-customer#deploy-the-azure-resource-manager-templates).
	
## **Recommended Documents**

* [How to onboard customer & gather-tenant-and-subscription-details](https://docs.microsoft.com/azure/lighthouse/how-to/onboard-customer#gather-tenant-and-subscription-details)
* [Create an Azure resource manager template](https://docs.microsoft.com/azure/lighthouse/how-to/onboard-customer#create-an-azure-resource-manager-template)
* [Deploy the Azure resource manager template](https://docs.microsoft.com/azure/lighthouse/how-to/onboard-customer#deploy-the-azure-resource-manager-templates)
* [Sample repo for Azure resource manager template](https://github.com/Azure/Azure-Lighthouse-samples/)
