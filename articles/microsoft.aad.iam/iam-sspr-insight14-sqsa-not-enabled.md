<properties
    pageTitle="Security questions are not enabled for password reset"
    description="Security questions are not enabled for password reset"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="sadiehenry"
    ms.author="sahenry"
    displayOrder="1"
    articleId="IAM_SSPR_Security_Questions_Enabled_For_Password_Reset"
    selfHelpType="diagnostics"
    diagnosticScenario="health_diagnostic"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	ownershipId="AzureIdentity_B2B"
/>

# Security questions are not enabled for password reset
<!--issueDescription-->
Administrators of your Azure AD have not enabled security questions as an allowed method for a user to reset their forgotten password.
<!--/issueDescription-->

## **Recommended Steps**

To enable security questions:

1. Navigate to the **Azure Active Directory** page in the Azure portal, then select **Password reset** and **Authentication methods**
2. Select the checkbox to enable **Security questions**
3. Configure the security questions that will be available for end users to reset their forgotten passwords, and click **Save**


## **Recommended Documents**

* [Quickstart for self-service password reset](https://docs.microsoft.com/azure/active-directory/authentication/quickstart-sspr)
