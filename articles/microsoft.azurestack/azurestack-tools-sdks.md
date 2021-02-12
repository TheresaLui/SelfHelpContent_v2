<properties
    pageTitle="Azure Stack Software Development Kit (SDK) and Visual Studio Integration"
    description="Azure Stack Software Development Kit (SDK) and Visual Studio Integration"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629278"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="azurestack-tools-sdks"
	ownershipId="StorageMediaEdge_AzureStack_Hub"
/>

# Azure Stack Software Development Kit (SDK) and Development Tools

The Azure Stack Software Development Kit (SDK) provides code samples for common languages so that you can build solutions that work with Azure Stack resource providers. In the SDK, you can find code samples to help you integrate your solution with your preferred language with Azure Stack by using profiles.

You can also use Visual Studio or [Azure DevOps Services](https://docs.microsoft.com/azure/devops/user-guide/what-happened-vsts?view=vsts) to develop Azure Resource Manager templates and deploy them to Azure Stack.

**Note**: If you are a looking for the Azure Stack Development Kit (ASDK), the single-node version of Azure Stack for evaluating Azure Stack and developing solutions for Azure Stack, please refer to the [ASDK documentation](https://docs.microsoft.com/azure/azure-stack/asdk/).

## **Recommended Steps**

1. To use supported PowerShell cmdlets with your Azure Stack environment, [Install Azure Stack PowerShell](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-powershell-install) and [Connect to Azure Stack with PowerShell as a user](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-powershell-configure-user)
2. Start developing using the sample provided for the language you would like to work with, including [.NET](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-version-profiles-net), [GO](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-version-profiles-go), [Ruby](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-version-profiles-ruby), [Python](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-version-profiles-python), or API version profiles for [PowerShell](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-version-profiles-powershell) and [Azure CLI](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-version-profiles-azurecli2)
3. Gather the required information from your Azure Stack environment, including **Tenant ID**, **Client ID**, **Subscription ID**, **Client Secret**, and [**Resource Manager Endpoint**](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-version-profiles-ruby#the-azure-stack-resource-manager-endpoint)
4. If you are using Visual Studio to develop and deploy to Azure Stack, follow steps to:

    - [Connect to Azure Stack with Azure AD](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-install-visual-studio#connect-to-azure-stack-with-azure-ad)
    - [Connect to Azure Stack with AD FS](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-install-visual-studio#connect-to-azure-stack-with-ad-fs)

## **Recommended Documents**

- [Develop for Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-developer)
- [Manage and deploy resources to Azure Stack Hub with Azure CLI](https://docs.microsoft.com/azure-stack/user/azure-stack-version-profiles-azurecli2)
- [Develop templates for Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-develop-templates)
- [Manage API version profiles in Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-version-profiles)
- [Resource provider API versions supported by profiles in Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-profiles-azure-resource-manager-versions)
