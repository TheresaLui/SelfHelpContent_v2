<properties
    pageTitle="Saml response sent to invalid reply url local host"
    description= "For custom application's configured in azure active directory and configured for saml single sign-on, the saml response is sent to reply url local host"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    infoBubbleText="See details on the right"
    authors="zabenamr"
    authorAlias="zabenamr"
    displayOrder=""
    supportTopicIds=""
    selfHelpType="diagnostics"
    diagnosticScenario="InvalidReplyUrlLocalHost"
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
    articleId="enterpriseapps_samlsso_invalid_replyUrl"
    />

# Saml request is being sent to reply url https://127.0.0.1:444/applications/default.aspx

## **Recommended steps**

1.	Sign-in into Azure portal as a Global administrator or another role that is able to manage this application.
2.	Navigate to Azure Active Directory, and click on App registrations
3.	Select All Apps view and search for your application. Then, on the application page click on Settings.
4.	On the menu, click on Reply URLs to view all the reply URLs configured for the application.
5.	Delete the https://127.0.0.1:444 URL and save.