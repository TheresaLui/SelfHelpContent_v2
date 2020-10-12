<properties
    pageTitle="Password writeback is not working"
    description="Password writeback is not working"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="sadiehenry"
    ms.author="sahenry"
    displayOrder="1"
    articleId="IAM_SSPR_Writeback_Not_Working"
    selfHelpType="diagnostics"
    diagnosticScenario="health_diagnostic"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	ownershipId="AzureIdentity_B2B"
/>

# Password Writeback is Not Working
<!--issueDescription-->
User <!--$UserId-->[UserId]<!--/$UserId--> is not able to change or reset their password because password writeback is not currently working in your Azure AD.
<!--/issueDescription-->

## **Recommended Steps**

To check the status of password writeback in your Azure AD:

1. Navigate to the *Azure Active Directory* page in the Azure portal, then select *Password reset*
2. Select *On-premises integration* to see the status of password writeback capabilities for your Azure AD

To troubleshoot and fix this issue, follow the [password writeback troubleshooting guide](https://docs.microsoft.com/azure/active-directory/authentication/active-directory-passwords-troubleshoot#troubleshoot-password-writeback).

## **Recommended Documents**

* Learn more about [password writeback](https://docs.microsoft.com/azure/active-directory/authentication/concept-sspr-writeback)
