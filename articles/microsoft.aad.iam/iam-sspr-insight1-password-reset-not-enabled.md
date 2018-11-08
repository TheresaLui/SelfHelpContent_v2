<properties
    pageTitle="Self-service password reset is not enabled"
    description="Self-service password reset is not enabled"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="sadiehenry"
    displayOrder="1"
    articleId="Password_Reset_Not_Enabled"
    selfHelpType="diagnostics"
    diagnosticScenario="health_diagnostic"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>

# Self-service password reset not enabled

We have determined that self-service password reset is not enabled for your tenant <!--$TenantId-->[TenantId]<!--/$TenantId-->. This means that users who do not have an administrator role cannot reset their passwords on their own. To enable self-service password reset, do the following:

1. From your Azure AD tenant, on the *Azure portal* under *Azure Active Directory*, select *Password reset*.
2. From the *Properties* page, under the option *Self Service Password Reset Enabled*, choose *Selected* or *All*.

For more guidance on configuring self-service password reset, review the [Quickstart for self-service password reset](https://docs.microsoft.com/azure/active-directory/authentication/quickstart-sspr).
