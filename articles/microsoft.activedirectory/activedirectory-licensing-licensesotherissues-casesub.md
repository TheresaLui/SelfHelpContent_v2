<properties
    pageTitle="Other issues with licenses"
    description="Other issues with licenses"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="piotrci"
    displayOrder="1770"
    supportTopicIds="32570962"
    selfHelpType="generic"
    resourceTags=""
    productPesIds="14785"
    cloudEnvironments="public"
 />

# Other issues with licenses

**Things to check first**
1. Is your problem related to per-user subscriptions (e.g. Office 365, Enterprise Mobility + Security, Dynamics 365, etc.) or an Azure resource subscription (e.g. virtual machines, storage accounts)? For Azure resource subscription problems, make sure to open the support ticket under "Subscription problems".

2. To manage licenses on groups, you must use an account with one of the required [administrator roles](https://docs.microsoft.com/azure/active-directory/active-directory-assign-admin-roles): Global Administrator or User Administrator. You can check the user’s role in the **Directory role** tab on the user blade.

3. If you are using the Azure portal and license assignment is failing, make sure to click the notification in the upper-right corner. This opens a blade with details about what went wrong. In most cases that is enough to understand and resolve the problem.

## **Recommended steps**

The [Azure portal](https://portal.azure.com/) does not require an Azure resource subscription to access.

- If you are looking to create a report of how licenses are assigned to users in your tenant, you must use a PowerShell script to download individual user data and process it locally. 

- You can use PowerShell cmdlets from version 1.0 (e.g. [Get-MsolUser](https://docs.microsoft.com/powershell/module/msonline/get-msoluser?view=azureadps-1.0)) or version 2.0 (e.g. [Get-​Azure​AD​User​License​Detail](https://docs.microsoft.com/powershell/module/azuread/Get-AzureADUserLicenseDetail?view=azureadps-2.0)).
