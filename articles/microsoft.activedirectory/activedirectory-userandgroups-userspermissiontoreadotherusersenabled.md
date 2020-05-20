<properties
    pageTitle="UsersPermissionToReadOtherUsersEnabled is false"
    description="Adding internal/external members to teams in Microsoft Teams fails when UsersPermissionToReadOtherUsersEnabled is set to false"
    infoBubbleText="An issue has been found that could cause problems with adding internal/external members to teams in Microsoft Teams. See details on the right."
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="adhavle"
    ms.author="adhavle"
    articleId="activedirectory-userandgroups-userspermissiontoreadotherusersenabled"
    diagnosticScenario="UsersPermissionToReadOtherUsersInsight"
    selfHelpType="diagnostics"
    supportTopicIds="32447987"
    resourceTags=""
    productPesIds="16579"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	ownershipId="AzureIdentity_MultiFactorAuthentication"
/>

# Configuration Issue Causing Failure To Add Internal/External Members In Microsoft Teams

<!--issueDescription-->
Adding internal/external members to teams in Microsoft Teams fails when **UsersPermissionToReadOtherUsersEnabled** is set to "false". This setting applies company-wide and can be disabled by administrators in order to disable users from viewing profile information of other users in their company. If that was not the intent, follow the steps below to enable this setting.
<!--/issueDescription-->

## **Recommended Steps**

1. Connect to AzureAD using [Azure PowerShell](https://docs.microsoft.com/powershell/azure/active-directory/overview?view=azureadps-1.0) with the command `Connect-MsolService`
2. Set **UsersPermissionToReadOtherUsersEnabled** to "true" using [Set-MsolCompanySettings](https://docs.microsoft.com/powershell/module/msonline/Set-MsolCompanySettings?view=azureadps-1.0): `Set-MsolCompanySettings -UsersPermissionToReadOtherUsersEnabled $true`
3. Verify the setting: `Get-MsolCompanyInformation`

## **Recommended Documents**

* [Known issues for Microsoft Teams](https://docs.microsoft.com/microsoftteams/known-issues)
