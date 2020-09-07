<properties 
    pageTitle="I can't assign licenses to a user or group"
    description="I can't assign licenses to a user or group"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="piotrci"
    ms.author="piotrci"
    displayOrder="27"
    supportTopicIds=""
    selfHelpType="resource"
    resourceTags="licensing_overview"
    productPesIds=""
    cloudEnvironments="MoonCake"
 	articleId="activedirectory-licensing-cant-assign-mooncake"
	ownershipId="AzureIdentity_User"
/>

# I can't assign licenses to a user or group

## **Recommended Steps**

To manage user licenses, you must use an account with one of the required [administrator roles](https://docs.azure.cn/active-directory/users-groups-roles/directory-assign-admin-roles): Global Administrator or User Administrator. You can check the user’s role in the **Directory role** tab on the user blade.

Here are some helpful tips for diagnosing problems with license assignment:

1. If you are using the Azure portal and license assignment is failing, select the notification in the upper-right corner. This opens a blade with details about what went wrong, including the common problem cases listed here.

2. Before a license can be assigned to a user, the Usage Location property must be set for the user. Verify the user has that property set by viewing the **Profile** property on the user blade.

3. Make sure there are enough available licenses for the product you are trying to assign. You can see the number of available licenses in the Azure portal, at [Azure Active Directory-&gt;Licenses-&gt;All products](https://portal.azure.cn/#blade/Microsoft_AAD_IAM/LicensesMenuBlade/Products).

4. The user may already have another license whose services conflict with the those in the new license you are trying to assign. For example, if the user has the *Exchange Online (Plan 1)* service enabled, you won’t be able to assign a license with the *Exchange Online (Plan 2)*. One of the services must be disabled to allow the new license assignment. If you are using the Azure portal or PowerShell cmdlets, the problem details page lists the specific services that are causing the conflict.

5. If you are trying to remove a license and that is failing, the user might have other licenses with services that depend on the services you are trying to remove. If you are using the Azure portal or PowerShell cmdlets, the problem details page lists the specific services that have dependencies.
