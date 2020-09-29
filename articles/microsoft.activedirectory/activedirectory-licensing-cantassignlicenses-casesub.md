<properties
    pageTitle="I can't assign licenses to a user"
    description="I can't assign licenses to a user"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="SumitParikh"
    ms.author="sumitp"
    displayOrder="1770"
    supportTopicIds="32570959"
    selfHelpType="generic"
    resourceTags=""
    productPesIds="16578"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
 	articleId="a80b47b3-fdc3-4933-b1f9-31fab817fe04"
	ownershipId="AzureIdentity_DirectoryObjectManagement"
/>

# I can't assign licenses to a user

**Prerequisites**

1. To manage user licenses, you must use an account with one of the required [administrator roles](https://docs.microsoft.com/azure/active-directory/active-directory-assign-admin-roles): Global Administrator, License Administrator, or User Administrator. You can check the user’s role in the **Directory role** tab on the user blade.
2. If you are using the Azure portal and license assignment is failing, make sure to click the notification in the upper-right corner. This opens a blade with details about what went wrong. In most cases that is enough to understand and resolve the problem.

## **Recommended Steps**

1. Before a license can be assigned to a user, the Usage Location property must be set for the user. Verify the user has that property set by viewing the **Profile** tab on the user blade.
2. Make sure there are enough available licenses for the product you are trying to assign. You can see the number of available licenses in the Azure portal, at [Azure Active Directory-&gt;Licenses-&gt;All products](https://portal.azure.com/#blade/Microsoft_AAD_IAM/LicensesMenuBlade/Products).
3. The user may already have another license whose services conflict with the those in the new license you are trying to assign. For example, if the user has the *Exchange Online (Plan 1)* service enabled, you won’t be able to assign a license with the *Exchange Online (Plan 2)*. One of the services must be disabled to allow the new license assignment. If you are using the Azure portal or PowerShell cmdlets, the problem details page lists the specific services that are causing the conflict.
4. If you are trying to remove a license and that is failing, the user might have other licenses with services that depend on the services you are trying to remove. If you are using the Azure portal or PowerShell cmdlets, the error message will list the specific services that have dependencies.
5. If you want to understand why a license was added/removed from a user (e.g. who else in your organization may have made changes) check the audit logs. Set the filter to **license activities** to show all modifications including the "actor" that performed them.
6. If you are using Exchange Online, some users in your tenant may be incorrectly configured with the same proxy address value. In such cases, you may see generic error messages when license operation fails. [This article](https://support.microsoft.com/help/3042584/-proxy-address-address-is-already-being-used-error-message-in-exchange-online) contains more information about this problem,  including information on [how to connect to Exchange Online using remote PowerShell](https://technet.microsoft.com/library/jj984289.aspx).
To identify which users in your tenant, contain the same proxy address, execute this Exchange Online cmdlet:

```
Run

Get-Recipient | where {$_.EmailAddresses -match <user principal name>} | fL Name, RecipientType,emailaddresses
```
