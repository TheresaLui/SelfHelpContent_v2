<properties
  pagetitle="Azure Stack APIs"
  service="microsoft.azurestack"
  resource="registrations"
  ms.author="alexsmit,justinha"
  selfhelptype="Generic"
  supporttopicids="32629200,32737127,32737265,32745852"
  resourcetags=""
  productpesids="16226,17058,17057,17322"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="azurestack-tools-apis"
  ownershipid="StorageMediaEdge_AzureStack_Hub" />
# Azure Stack APIs

Azure Stack has a variety of APIs for cloud admins and tenant users to access Azure Stack environments:

* **Azure Stack Admin REST API** for each Resource Provider that ships with Azure Stack, for performing operations on resource objects such as Scale Unit Nodes, Alerts, Updates, Backup, Marketplace, Subscriptions, and Offers
* **Resource provider APIs** for each resource provider [supported by profiles in Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-profiles-azure-resource-manager-versions). Each client uses an API profile to contact the correct resource provider and API version for Azure Stack.
* **Azure CLI** is a command-line tool for managing Azure Stack resources, designed to enable scripting, querying data, performing long-running operations, and more
* **Azure PowerShell** cmdlets use the Azure Resource Manager model for managing Azure resources. [Azure Stack PowerShell](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install) uses API profiles to ensure that you are using the right resource provider and version when using cmdlets.

## **Recommended Steps**

### Azure Stack Admin REST API

1. See [how to call Azure REST APIs](https://docs.microsoft.com/rest/api/azure/) for setting up authentication, your client, and the flow for sending a request and receiving a return payload
1. After connecting, follow the steps to [use the Azure Stack API](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-rest-api-use)

### Azure Stack Resource Providers APIs

1. Identify the desired resource provider in [supported by profiles in Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-profiles-azure-resource-manager-versions)
1. Find the specific call that you want to make by consulting the [Azure Stack Rest API Reference](https://docs.microsoft.com/rest/api/azure-stack)
1. To submit the request, follow the steps to [use the Azure Stack API](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-rest-api-use)

### Azure CLI

- Configure your environment and connect to Azure Stack [using API version profiles with Azure CLI](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-version-profiles-azurecli2)

### Azure PowerShell

1. Uninstall [existing versions of the Azure Stack PowerShell modules](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install?toc=/azure/azure-stack/user/TOC.json#3-uninstall-existing-versions-of-the-azure-stack-powershell-modules)
1. Install [PowerShell for Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install) on your client machine
1. Verify the [installed API profile](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-version-profiles-powershell#get-the-installed-profiles) and ARM context for your environment
1. Connect to [Azure Stack with PowerShell as an operator](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-configure-admin) to perform Azure Stack administration tasks

## **Recommended Documents**

* [Azure Stack Admin API reference](https://docs.microsoft.com/rest/api/azure-stack/)<br>
* [Resource provider API versions supported by profiles in Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-profiles-azure-resource-manager-versions)<br>
* [Azure CLI in Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-version-profiles-azurecli2)<br>
* [Overview of Azure PowerShell](https://docs.microsoft.com/powershell/azure/overview?view=azurermps-6.12.0)<br>
* [Manage API version profiles in Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-version-profiles)
