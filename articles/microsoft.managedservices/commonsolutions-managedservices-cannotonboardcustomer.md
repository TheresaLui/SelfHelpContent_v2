<properties
  pagetitle="Cannot onboard customer&#xD;"
  description="Cannot onboard customer"
  service=""
  resource=""
  ms.author="prukulka,sezhen"
  selfhelptype="Generic"
  supporttopicids="32642166"
  resourcetags=""
  productpesids="16761"
  cloudenvironments="fairfax,mooncake,public,usnat,ussec,blackforest"
  disableclouds=""
  articleid="commonsolutions-managedservices-cannotonboardcustomer-cantfindids"
  ownershipid="Compute_AzureLighthouse" />
# Cannot onboard customer

Most users are able to resolve their customer onboarding to Lighthouse issue using the steps below.

## **Recommended Steps**

**Can't deploy template successfully?**

- To onboard your customer, you'll need to create an [Azure Resource Manager](https://docs.microsoft.com/azure/azure-resource-manager/index) template for your offer with the following information. The mspOfferName and mspOfferDescription values will be visible to the customer when viewing offer details in the [Service providers page](https://docs.microsoft.com/azure/lighthouse/how-to/view-manage-service-providers) of the Azure portal.
- The onboarding process requires an Azure Resource Manager template (provided in our [samples repo](https://github.com/Azure/Azure-Lighthouse-samples/) and a corresponding parameters file that you modify to match your configuration and define your authorizations
- Watch this [demo](https://www.microsoft.com/azure/partners/videos/how-to-onboard-to-a-service-provider-using-arm-templates-in-azure-lighthouse) on how to onboard via ARM templates. 
- Try our common [troubleshooting tips](https://docs.microsoft.com/azure/lighthouse/how-to/onboard-customer#troubleshooting).

**Can't deploy template at resource group level?**

- Deployments must be performed at the subscription level by a non-guest account in the customer's tenant who has the Owner built-in role for the subscription being onboarded (or which contains the resource groups that are being onboarded). This deployment can't be initiated in the Azure portal, but can be done by using PowerShell or Azure CLI, as shown in [Deploy the Azure Resource Manager templates](https://docs.microsoft.com/azure/lighthouse/how-to/onboard-customer#deploy-the-azure-resource-manager-templates).
	
## **Recommended Documents**

* [How to onboard customer & gather-tenant-and-subscription-details](https://docs.microsoft.com/azure/lighthouse/how-to/onboard-customer#gather-tenant-and-subscription-details)
* [Create an Azure resource manager template](https://docs.microsoft.com/azure/lighthouse/how-to/onboard-customer#create-an-azure-resource-manager-template)
* [Deploy the Azure resource manager template](https://docs.microsoft.com/azure/lighthouse/how-to/onboard-customer#deploy-the-azure-resource-manager-templates)
* [Sample repo for Azure resource manager template](https://github.com/Azure/Azure-Lighthouse-samples/)