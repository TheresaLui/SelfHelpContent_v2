<properties
    pageTitle="Password writeback is not working"
    description="Password writeback is not working"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="sadiehenry"
    displayOrder="1"
    articleId="IAM_SSPR_Writeback_Not_Working"
    selfHelpType="diagnostics"
    diagnosticScenario="health_diagnostic"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>

# Password writeback is not working

We have determined that <!--$UserId-->[UserId]<!--/$UserId--> in your tenant: <!--$TenantId-->[TenantId]<!--/$TenantId--> is not able to change or reset their password because password writeback is not currently working in your tenant.

To check the status of password writeback in your tenant, do the following:

1. From your Azure AD tenant, on the *Azure portal* under *Azure Active Directory*, select *Password reset*.
2. From the *On-premises integration* page, view the status of password writeback.

To troubleshoot and fix this issue, follow the [password writeback troubleshooting guide](https://docs.microsoft.com/azure/active-directory/authentication/active-directory-passwords-troubleshoot#troubleshoot-password-writeback).
 
Learn more about [password writeback](https://docs.microsoft.com/azure/active-directory/authentication/concept-sspr-writeback)
