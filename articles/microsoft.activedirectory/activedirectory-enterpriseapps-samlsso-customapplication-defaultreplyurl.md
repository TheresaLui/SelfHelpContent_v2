<properties
    pageTitle="Saml response sent to invalid reply url local host"
    description= "For custom application's configured in azure active directory and configured for saml single sign-on, the saml response is sent to reply url local host"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    infoBubbleText="See details on the right"
    authors="zabenamr"
    ms.author="zabenamr"
    displayOrder=""
    supportTopicIds=""
    selfHelpType="diagnostics"
    diagnosticScenario="InvalidReplyUrlLocalHost"
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    articleId="enterpriseapps_samlsso_invalid_replyUrl"
    	ownershipId="AzureIdentity_User"
/>

# SAML Request is being sent to Reply URL https://127.0.0.1:444/applications/default.aspx
<!--/issueDescription-->
The SAML Request is being sent to an invalid Reply URL.
<!--/issueDescription-->

## **Recommended Steps**

1. Sign in to [Azure portal](https://portal.azure.com) as a Global administrator or any other role that is able to manage this application
2. Navigate to Azure Active Directory and click on "App registrations"
3. Change your view to "All Apps" and search for your application
4. Click "Settings" on your application page
5. In the menu, click on "Reply URLs" to view all the reply URLs configured for the application
6. Locate the https://127.0.0.1:444 URL and delete it
7. Click "Save"
