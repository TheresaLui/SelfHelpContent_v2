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

Azure Stack has a variety of APIs for cloud admins and tenant users to access the Azure Stack environment-

- **Azure Stack Admin REST API** for each Resource Provider that ships with Azure Stack inbox, for performing operations on selected entities such as Scale Unit Nodes, Alerts, Updates, Backup, Marketplace, Subscriptions, Offers, and more.
- **Resource provider APIs** for each resource provider with [supported by profiles in Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-profiles-azure-resource-manager-versions). Each client uses an API profile to contact the correct resource provider and API version for Azure Stack.
- **Azure CLI** command-line tool for managing Azure Stack resources designed to enable scripting, query data, support long-running operations, and more.
- **Azure PowerShell**, a set of cmdlets that use the Azure Resource Manager model for managing your Azure resources. [Azure Stack Powershell](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install) uses API profiles to ensure you are using the right resource provider and version when using cmdlets.

## **Recommended Steps**

### **Azure Stack Admin REST API**

1. Review [how to call Azure REST APIs](https://docs.microsoft.com/rest/api/azure/) for steps on setting up authorization, your client, and the flow for sending a request and receiving a return payload
2. Follow steps to [use the Azure Stack API](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-rest-api-use)

### **Azure Stack Resource Providers APIs**

1. Identify the desired resource provider with [supported by profiles in Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-profiles-azure-resource-manager-versions)
2. Find the specific call you would like to me by consulting the [Azure Stack Rest API Reference](https://docs.microsoft.com/rest/api/azure-stack)
3. Follow steps to [use the Azure Stack API](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-rest-api-use)

### **Azure PowerShell**

1. Make sure to [uninstall existing versions of the Azure Stack PowerShell modules](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install?toc=/azure/azure-stack/user/TOC.json#3-uninstall-existing-versions-of-the-azure-stack-powershell-modules), and check that you are using correct API Profile
2. [Install PowerShell for Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install) on your client machine
3. Check your [installed profiles](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-version-profiles-powershell#get-the-installed-profiles) and ARM context for your environment
4. [Connect to Azure Stack with PowerShell as an operator](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-configure-admin) to perform Azure Stack administration tasks

### **Azure CLI**

1. [Install Azure CLI](https://docs.microsoft.com/cli/azure/install-azure-cli) on your development workstation
2. [Enable Azure CLI for Azure Stack users](https://docs.microsoft.com/azure/azure-stack/azure-stack-cli-admin)
3. [Use API version profiles with Azure CLI in Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-version-profiles-azurecli2) to configure your environment and connect to Azure Stack

## **Recommended Documents**

- [Azure Stack Admin API reference](https://docs.microsoft.com/rest/api/azure-stack/)
- [Resource provider API versions supported by profiles in Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-profiles-azure-resource-manager-versions)
- [Overview of Azure PowerShell](https://docs.microsoft.com/powershell/azure/overview?view=azurermps-6.12.0)
- [Manage API version profiles in Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-version-profiles)