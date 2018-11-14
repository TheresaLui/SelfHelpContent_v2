<properties
    pageTitle="Enterprise Application - Config issue preventing user sign-in"
    description="Enterprise Application - Config issue preventing user sign-in"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="asbh"
    displayOrder="1"
    articleId="Application_SignIn_ADSTS_50011"
    diagnosticScenario="EnterpriseApps"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>

# Enterprise Application - Config issue preventing user sign-in

The Authentication request (SAML request) that you are sending does not have the correct reply URL. This will prevent any user from accessing this application.

In order to enable user sign-in for this application, please follow the steps below:

**Step 1**: Sign in to the Azure Portal as a global administrator or another role that is able to manage this application.

**Step 2**: Navigate to the Azure Active Directory, and go to the Enterprise applications blade. Search for the application for which you want to enable federated single sign-on.

**Step 3**: Click on the application name to open it. Then, on the application's left-hand navigation menu, click "Single Sign-On".

**Step 4**: Under the Domain and URLs section, update or enter the Reply URL (ACS URL) in Azure AD with the correct value <!--$ReplyUrl-->ReplyUrl<!--/$ReplyUrl-->. If you don’t see a Reply URL field, please check the "Show Advance URL settings" section.

Your application should now be available for user sign-in.

For more information on common application-related issues, please refer to the following document: <!--$AppSignInErrorHelpPage-->AppSignInErrorHelpPage<!--/$AppSignInErrorHelpPage-->