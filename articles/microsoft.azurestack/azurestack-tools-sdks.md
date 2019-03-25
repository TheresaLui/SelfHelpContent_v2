<properties
    pageTitle="Azure Stack Software Development Kit (SDK) and Visual Studio Integration"
    description=""
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629278"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public"
    articleId="azurestack-tools-sdks"
/>

# Azure Stack Software Development Kit (SDK)

Azure Stack provides code samples in a Software Development Kit (SDK) for common languages so that you can build solutions that work with the Azure Stack resource providers using version profiles. The SDK will revert to the correct API version so that you can create an app to work with Azure resource providers without having to sort out exactly which version of each resource provider API is compatible with Azure Stack.<br>

**Note**: If you are a looking for the Azure Stack Development Kit (ASDK), the kit provides a single-node version of Azure Stack for evaluating Azure Stack and developing solutions for Azure Stack. The kit however doesn't include code samples, development resources, or tools. You can find more information in the [ASDK documentation](https://docs.microsoft.com/azure/azure-stack/asdk/).<br>

In the SDK, You can find code samples to help you integrate your solution with your preferred language with Azure Stack by using profiles. You can find guidance and samples for the following languages:<br>

- **.NET**<br>
    You can use the .NET API profile to get the latest, most stable version of each resource type in a resource provider package. For more information, see [Use API version profiles with .NET in Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-version-profiles-net).<br>

- **PowerShell**<br>
    You can use the  **AzureRM.Bootstrapper** module available through the PowerShell Gallery to get the PowerShell cmdlets required to work with API version profiles. For information, see [Use API version profiles for PowerShell](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-version-profiles-powershell).<br>

- **Azure CLI**<br>
    You can update your environment configuration to use the Azure Stack specific API version profile. For information, see [Use API version profiles for Azure CLI](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-version-profiles-azurecli2).<br>

- **GO**<br>
    In the GO SDK, a profile is a combination of different resource types with different versions from different services. profiles are available under the profiles/ path, with their version in the **YYYY-MM-DD** format. For information, see [Use API version profiles for GO](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-version-profiles-go).<br>

- **Ruby**<br>
    The Ruby SDK for the Azure Stack Resource Manager provides tools to help you build and manage your infrastructure. Resource providers in the SDK include compute, virtual networks, and storage with the Ruby language. For information, see [Use API version profiles with Ruby](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-version-profiles-ruby).<br>

- **Python**<br>
    The Python SDK supports API version profiles to target different cloud platforms such as Azure Stack and global Azure. You can use API profiles in creating solutions for a hybrid cloud. For information, see [Use API version profiles with Python](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-version-profiles-python).<br>

## **Recommended steps**

1. Visit the sample of the language you would like to work with.<br>
2. Install the prerequisites and get the required information from your Azure Stack environment. For example, you will need:<br>
    - **Tenant ID**<br>
    The value of your Azure Stack tenant ID.<br>
    - **Client ID**<br> 
    The service principal application ID saved when service principal was created on the previous section of this document.<br>
    - **Subscription ID**<br>
    The subscription ID is how you access offers in Azure Stack.<br>
    - **Client Secret**<br>
    The service principal application Secret saved when service principal was created.<br>
    - **Resource Manager Endpoint**<br>
    [The Azure Stack resource manager endpoint](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-version-profiles-ruby#the-azure-stack-resource-manager-endpoint).<br>
3. Update the code sample with the required values, and run.<br>

## **Recommended documents**

[Manage API version profiles in Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-version-profiles)<br>
[Resource provider API versions supported by profiles in Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-profiles-azure-resource-manager-versions)

# Azure Stack and Visual Studio

Note: [Visual Studio Team Services is now Azure DevOps Services](https://docs.microsoft.com/azure/devops/user-guide/what-happened-vsts?view=vsts)<br>

You can use Visual Studio to write and deploy Azure Resource Manager templates to Azure Stack.<br>

## **Recommended steps**

1. [Install Visual Studio](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-install-visual-studio#install-visual-studio).<br>
2. [Install Azure Stack PowerShell](https://docs.microsoft.com?azure/azure-stack/user/azure-stack-powershell-install).<br>
3. If you are using a machine outside of the Azure Stack and you are using Azure Stack Development Kit (ASDK), you can establish [a split tunnel Virtual Private Network (VPN) connection](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-connect-azure-stack#connect-to-azure-stack-with-vpn).<br>
1. Connect to Azure Stack through Visual Studio.<br>
    1. [Connect to Azure Stack with Azure AD](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-install-visual-studio#connect-to-azure-stack-with-azure-ad)<br>
    1. [Connect to Azure Stack with AD FS](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-install-visual-studio#connect-to-azure-stack-with-ad-fs)<br>


## **Recommended documents**

[Visual Studio documentation](https://docs.microsoft.com/visualstudio/?view=vs-2017)<br>
[Develop for Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-developer)<br>
[Develop templates for Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-develop-templates)