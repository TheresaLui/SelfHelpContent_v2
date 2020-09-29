<properties
    pageTitle="User is blocked"
    description="User is blocked"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="sadiehenry"
    ms.author="sahenry"
    displayOrder="1"
    articleId="IAM_SSPR_User_Blocked"
    selfHelpType="diagnostics"
    diagnosticScenario="health_diagnostic"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	ownershipId="AzureIdentity_B2B"
/>

# User is blocked
<!--issueDescription-->
Administrators in your Azure AD have not enabled <!--$UserId-->[UserId]<!--/$UserId--> to reset their own forgotten password.
<!--/issueDescription-->

## **Recommended Steps**

To enable <!--$UserId-->[UserId]<!--/$UserId--> for self-service password reset:

1. Navigate to the **Azure Active Directory** page in the Azure portal, then select **Password reset** and **Properties**
2. In the section for **Self Service Password Reset Enabled**, choose **Selected**, and select a group in which <!--$UserId-->[UserId]<!--/$UserId--> is a member or choose **All** to enable self-service password reset for all users in your Azure AD

## **Recommended Documents**

* To unblock this user, follow the instructions listed in [this article](https://docs.microsoft.com/azure/active-directory/identity-protection/howto-unblock-user)
