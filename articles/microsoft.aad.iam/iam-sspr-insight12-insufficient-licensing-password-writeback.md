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
    cloudEnvironments="public"
/>

# Insufficient licensing for password writeback
<!--/issueDescription-->
Your tenant <!--$TenantId-->[TenantId]<!--/$TenantId--> does not have the appropriate licensing required for password writeback. <!--$UserId-->[UserId]<!--/$UserId--> is a hybrid user, therefore, password writeback must be enabled and licensing acquired before they can change or reset their password.
<!--/issueDescription-->

## **Recommended Steps**

* Review the [password reset licensing requirements](https://docs.microsoft.com/azure/active-directory/authentication/concept-sspr-licensing) to determine which license(s) you need
