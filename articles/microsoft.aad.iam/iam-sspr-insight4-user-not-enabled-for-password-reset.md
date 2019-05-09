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
    cloudEnvironments="public"
/>

# User is not enabled for self-service password reset
<!--/issueDescription-->
We have determined that <!--$UserId-->[UserId]<!--/$UserId--> in your tenant <!--$TenantId-->[TenantId]<!--/$TenantId--> has not been enabled for self-service password reset.
<!--/issueDescription-->

## **Recommended Steps**

To enable <!--$UserId-->[UserId]<!--/$UserId--> for self-service password reset:

1. From your Azure AD tenant, on the **Azure portal** under **Azure Active Directory**, select **Password reset**
2. From the **Properties** page, under the option **Self Service Password Reset Enabled**, choose **Selected** and select a group that <!--$UserId-->[UserId]<!--/$UserId--> is a member of, or choose **All** to enable self-service password reset for all users in your tenant

## **Recommended Documents**

* [Quickstart for self-service password reset](https://docs.microsoft.com/azure/active-directory/authentication/quickstart-sspr)
