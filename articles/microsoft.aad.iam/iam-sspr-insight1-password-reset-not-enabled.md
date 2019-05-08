<properties
    pageTitle="Self-service password reset is not enabled"
    description="Self-service password reset is not enabled"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    ms.author="sahenry"
    authors="sadiehenry"
    displayOrder="1"
    articleId="IAM_SSPR_Password_Reset_Not_Enabled"
    selfHelpType="diagnostics"
    diagnosticScenario="health_diagnostic"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>

# Self-service password reset not enabled
<!--/issueDescription-->
Self-service password reset is not enabled for your tenant <!--$TenantId-->[TenantId]<!--/$TenantId-->. Users who do not have an administrator role cannot reset their passwords on their own.
<!--/issueDescription-->

## **Recommended Steps**

To enable self-service password reset:

1. From your Azure AD tenant, in the **Azure portal** under **Azure Active Directory**, select **Password reset**
2. From the **Properties** page, under the option **Self Service Password Reset Enabled**, choose **Selected** or **All**

## **Recommended Documents**

* [Quickstart for self-service password reset](https://docs.microsoft.com/azure/active-directory/authentication/quickstart-sspr)
