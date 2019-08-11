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
    cloudEnvironments="public"
/>

# User is an administrator
<!--/issueDescription-->
User <!--$UserId-->[UserId]<!--/$UserId--> in your tenant <!--$TenantId-->[TenantId]<!--/$TenantId--> is an administrator. Microsoft enforces a strong two-gate password reset policy for any Azure administrator role. Administrators cannot register security questions. Please test your password reset policy with a user who is not an administrator.
<!--/issueDescription-->

## **Recommended Documents**

* [Administrator password reset policy](https://docs.microsoft.com/azure/active-directory/authentication/concept-sspr-policy#administrator-reset-policy-differences)
