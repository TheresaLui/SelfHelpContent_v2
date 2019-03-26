<properties
    pageTitle="Azure Stack APIs"
    description="Help with APIs available to Azure Stack"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629184,32629200"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public"
    articleId="azurestack-tools-apis"
/>

# Azure Stack APIs

Azure Stack has a variety of APIs for cloud admins and tenant users to access Azure Stack environments:

- **Azure Stack Admin REST API** for each Resource Provider that ships with Azure Stack, for performing operations on resource objects such as Scale Unit Nodes, Alerts, Updates, Backup, Marketplace, Subscriptions, Offers, and more
- **Resource provider APIs** for each resource provider [supported by profiles in Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-profiles-azure-resource-manager-versions). Each client uses an API profile to contact the correct resource provider and API version for Azure Stack.
- **Azure CLI** command-line tool for managing Azure Stack resources, designed to enable scripting, querying data, performing long-running operations, and more
- **Azure PowerShell** cmdlets that use the Azure Resource Manager model for managing Azure resources. [Azure Stack Powershell](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install) uses API profiles to ensure you are using the right resource provider and version when using cmdlets.

## **Recommended Steps**

### **Azure Stack Admin REST API**

1. Review [how to call Azure REST APIs](https://docs.microsoft.com/rest/api/azure/) for setting up authentication, your client, and the flow for sending a request and receiving a return payload
2. Once connected, follow steps to [use the Azure Stack API](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-rest-api-use)

### **Azure Stack Resource Providers APIs**

1. Identify the desired resource provider [supported by profiles in Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-profiles-azure-resource-manager-versions)
2. Find the specific call you would like to me by consulting the [Azure Stack Rest API Reference](https://docs.microsoft.com/rest/api/azure-stack)
3. To submit the request, follow steps to [use the Azure Stack API](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-rest-api-use)

### **Azure CLI**

1. [Install Azure CLI](https://docs.microsoft.com/cli/azure/install-azure-cli) on your client computer
2. [Enable Azure CLI for Azure Stack users](https://docs.microsoft.com/azure/azure-stack/azure-stack-cli-admin)
3. [Use API version profiles with Azure CLI in Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-version-profiles-azurecli2) to configure your environment and connect to Azure Stack

### **Azure PowerShell**

1. Make sure to [uninstall existing versions of the Azure Stack PowerShell modules](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install?toc=/azure/azure-stack/user/TOC.json#3-uninstall-existing-versions-of-the-azure-stack-powershell-modules)
2. [Install PowerShell for Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install) on your client machine
3. Verify your [installed API profile](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-version-profiles-powershell#get-the-installed-profiles) and ARM context for your environment
4. [Connect to Azure Stack with PowerShell as an operator](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-configure-admin) to perform Azure Stack administration tasks

## **Recommended Documents**

- [Azure Stack Admin API reference](https://docs.microsoft.com/rest/api/azure-stack/)
- [Resource provider API versions supported by profiles in Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-profiles-azure-resource-manager-versions)
- [Azure CLI in Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-version-profiles-azurecli2)
- [Overview of Azure PowerShell](https://docs.microsoft.com/powershell/azure/overview?view=azurermps-6.12.0)
- [Manage API version profiles in Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-version-profiles)
