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
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	ownershipId="AzureIdentity_B2B"
/>

# Self-service password reset not enabled
<!--issueDescription-->
Administrators of your Azure AD have not enabled self-service password reset for your users. Users who are not assigned to an administrator role in Azure AD cannot reset their own forgotten passwords.
<!--/issueDescription-->

## **Recommended Steps**

To enable self-service password reset for non-administrative users:

1. Navigate to the **Azure Active Directory** page in the Azure portal, then select **Password reset** and **Properties**
2. In the section for **Self Service Password Reset Enabled**, choose **Selected** or **All**

## **Recommended Documents**

* [Quickstart for self-service password reset](https://docs.microsoft.com/azure/active-directory/authentication/quickstart-sspr)
