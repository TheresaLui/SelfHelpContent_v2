<properties
    pageTitle="Saml response sent to reply url https://127.0.0.1:444/applications/default.aspx"
    description= "For custom application's configured in azure active directory and configured for saml single sign-on, the saml response is sent to reply url https://127.0.0.1:444/applications/default.aspx unexpectedly"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="zabenamr"
    displayOrder=""
    supportTopicIds=""
    selfHelpType="generic"
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
    articleId="enterpriseapps_samlsso_invalid_replyUrl"
    />

# Saml request is being sent to reply url https://127.0.0.1:444/applications/default.aspx

## Description
Application contains reply URL https://127.0.0.1:444/applications/default.aspx In some cases, we have noticed that the presence of this URL can cause interruptions to single sign-on. To avoid potential interruptions, we suggest you remove this reply URL from the application. Removing this reply URL will have no impact on users being able to access the application.

## Root Cause
When the application was added as a non-gallery app, Azure Active Directory created this reply URL as a default value. This behavior has changed and Azure Active Directory no longer adds this URL by default.

## Resolution Steps
1.	Sign-in into Azure portal as a Global administrator or another role that is able to manage this application.
2.	Navigate to Azure Active Directory, and click on App registrations
3.	Select All Apps view and search for <appName>. Then, on the application page click on Settings.
4.	On the menu, click on Reply URLs to view all the reply URLs configured for the application.
5.	Delete the https://127.0.0.1:444 URL and Save.
