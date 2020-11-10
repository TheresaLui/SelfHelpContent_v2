<properties
    pageTitle="User is not enabled for self-service password reset"
    description="User is not enabled for self-service password reset"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="sadiehenry"
    ms.author="sahenry"
    displayOrder="1"
    articleId="IAM_SSPR_User_Not_Enabled_For_Password_Reset"
    selfHelpType="diagnostics"
    diagnosticScenario="health_diagnostic"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	ownershipId="AzureIdentity_B2B"
/>

# User is not enabled for self-service password reset
<!--issueDescription-->
Administrators in your Azure AD have not enabled <!--$UserId-->[UserId]<!--/$UserId--> to reset their own forgotten password.
<!--/issueDescription-->

## **Recommended Steps**

To enable <!--$UserId-->[UserId]<!--/$UserId--> for self-service password reset:

1. Navigate to the **Azure Active Directory** page in the Azure portal, then select **Password reset** and **Properties**
2. In the section for **Self Service Password Reset Enabled**, choose **Selected**, and select a group in which <!--$UserId-->[UserId]<!--/$UserId--> is a member or choose **All** to enable self-service password reset for all users in your Azure AD

## **Recommended Documents**

* [Quickstart for self-service password reset](https://docs.microsoft.com/azure/active-directory/authentication/quickstart-sspr)
