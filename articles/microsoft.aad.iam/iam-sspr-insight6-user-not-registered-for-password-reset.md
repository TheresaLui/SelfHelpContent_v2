<properties
    pageTitle="User is not registered for self-service password reset"
    description="User is not registered for self-service password reset"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    ms.author="sahenry"
    authors="sadiehenry"
    displayOrder="1"
    articleId="IAM_SSPR_User_Not_Registered_For_Password_Reset"
    selfHelpType="diagnostics"
    diagnosticScenario="health_diagnostic"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	ownershipId="AzureIdentity_B2B"
/>

# User is not registered for self-service password reset
<!--issueDescription-->
User <!--$UserId-->[UserId]<!--/$UserId--> has not registered for self-service password reset in your Azure AD.
<!--/issueDescription-->

## **Recommended Steps**

* If <!--$UserId-->[UserId]<!--/$UserId-->  is able to sign in to your Azure AD, they can go to [mysignins.microsoft.com](https://mysignins.microsoft.com/security-info) to register for self-service password reset
* If <!--$UserId-->[UserId]<!--/$UserId--> is not able to sign in to your Azure AD, an administrator will need to reset this user's password and communicate the new password to the user. Then the user can sign in with their new password, and can register to use self-service password reset in the future.
