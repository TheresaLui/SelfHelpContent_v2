<properties
    pageTitle="Insufficient licensing for password writeback"
    description="Insufficient licensing for password writeback"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="sadiehenry"
    ms.author="sahenry"
    displayOrder="1"
    articleId="IAM_SSPR_Insufficient_Licensing_Password_Writeback"
    selfHelpType="diagnostics"
    diagnosticScenario="health_diagnostic"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	ownershipId="AzureIdentity_B2B"
/>

# Insufficient licensing for password writeback
<!--issueDescription-->
Your Azure AD does not have licenses required to use the password writeback capabilities of Azure AD. <!--$UserId-->[UserId]<!--/$UserId--> is a synchronized into Azure AD from your Windows Server AD.

In order for that user to change their password from the cloud, you must obtain the required licenses and enable password writeback for your Azure AD.
<!--/issueDescription-->

## **Recommended Steps**

* Review the [password reset licensing requirements](https://docs.microsoft.com/azure/active-directory/authentication/concept-sspr-licensing) to determine which license(s) you need
