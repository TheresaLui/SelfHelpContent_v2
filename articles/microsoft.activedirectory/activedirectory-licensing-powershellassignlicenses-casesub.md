<properties
    pageTitle="Issues managing licenses using PowerShell"
    description="Issues managing licenses using PowerShell"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="piotrci"
    displayOrder="1770"
    supportTopicIds="32570960"
    selfHelpType="generic"
    resourceTags=""
    productPesIds="14785"
    cloudEnvironments="public"
 />

# Issues managing licenses using PowerShell

**Things to check first**
1. Is your problem related to per-user subscriptions (e.g. Office 365, Enterprise Mobility + Security, Dynamics 365, etc.) or an Azure resource subscription (e.g. virtual machines, storage accounts)? For Azure resource subscription problems, make sure to open the support ticket under "Subscription problems".

2. There are two versions of PowerShell cmdlets for Azure AD that can be used for license management:
  * V2.0 contains cmdlets such as [Set-​Azure​AD​User​License](https://docs.microsoft.com/powershell/module/azuread/set-azureaduserlicense) and [Get-​Azure​AD​User​License​Detail](https://docs.microsoft.com/powershell/module/azuread/get-azureaduserlicensedetail).
  * V1.0 contains cmdlets such as [Set-​Msol​User​License](https://docs.microsoft.com/powershell/module/msonline/Set-MsolUserLicense) and [Get-​Msol​User](https://docs.microsoft.com/powershell/module/msonline/Get-MsolUser).
  * Useful examples of Office 365 license management with PowerShell v1.0 can be found [here](https://technet.microsoft.com/library/dn771770.aspx).

3. PowerShell support for [group-based licensing](https://docs.microsoft.com/azure/active-directory/active-directory-licensing-whatis-azure-portal) is currently limited, but some functionality is exposed via PowerShell v1.0 cmdlets. [See here for examples.](https://docs.microsoft.com/azure/active-directory/active-directory-licensing-ps-examples)

## **Recommended steps**

1. In some cases license operations may fail because of existing licenses assigned to the user. When investigating a problem with a user, open the user's blade in the Azure portal and select the **Licenses** tab; it contains complete information about the user's state, showing all currently assigned licenses, including the ones inherited from groups.

2. If you are using [group-based licensing](https://docs.microsoft.com/azure/active-directory/active-directory-licensing-whatis-azure-portal) in your tenant, note that it is [not possible to remove or modify inherited licenses](https://docs.microsoft.com/azure/active-directory/active-directory-licensing-group-advanced#direct-licenses-coexist-with-group-licenses) directly from a user. If you are getting an error when removing a license or disabling service plans on a license, view the user's **Licenses** tab to check if there is no inherited license on the user.

3. If you want to understand why a license was added/removed from a user or a group (e.g. who else in your organization may have made changes) make sure to view the [audit logs](https://portal.azure.com/#blade/Microsoft_AAD_IAM/LicensesMenuBlade/Audit). Setting the filter to license activities will show all modifications including the "actor" that performed them.

4. If you are using Exchange Online, some users in your tenant may be incorrectly configured with the same proxy address value. In such cases you may see generic error messages when license operation fails. [This article](https://support.microsoft.com/help/3042584/-proxy-address-address-is-already-being-used-error-message-in-exchange-online) contains more information about this problem,  including information on [how to connect to Exchange Online using remote PowerShell](https://technet.microsoft.com/library/jj984289.aspx).

  To identify which users in your tenant contain the same proxy address, execute this Exchange Online cmdlet:
```
Run Get-Recipient | where {$_.EmailAddresses -match <user principal name>} | fL Name, RecipientType,emailaddresses
```
