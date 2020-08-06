<properties
    pageTitle="User is an administrator"
    description="User is an administrator"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="sadiehenry"
    ms.author="sahenry"
    displayOrder="1"
    articleId="IAM_SSPR_User_Is_Admin"
    selfHelpType="diagnostics"
    diagnosticScenario="health_diagnostic"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	ownershipId="AzureIdentity_B2B"
/>

# User is an administrator
<!--issueDescription-->
User <!--$UserId-->[UserId]<!--/$UserId--> is an administrator of this Azure AD. An Azure AD administrator must pass a two-gate password reset process in order to reset their own forgotten password. Administrators cannot use security questions to reset their own password. If you are testing your self-service password reset policy, conduct that testing with a user who is not an Azure AD administrator.
<!--/issueDescription-->

## **Recommended Documents**

* [Administrator password reset policy](https://docs.microsoft.com/azure/active-directory/authentication/concept-sspr-policy#administrator-reset-policy-differences)
