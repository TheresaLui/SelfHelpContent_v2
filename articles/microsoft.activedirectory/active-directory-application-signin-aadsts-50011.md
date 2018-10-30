<properties
    pageTitle="Enterprise Application - Config issue preventing user sign-in"
    description="Enterprise Application - Config issue preventing user sign-in"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="asbh"
    displayOrder="1"
    articleId="Application_SignIn_ADSTS_50011"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>

# Enterprise Application - Config issue preventing user sign-in

Authentication request (SAML request) doesnt have the correct reply url. This will prevent any user from accessing this application.

In order to enable user sign-in for this application, please follow the steps below:

**Step1**: Sign-in to Azure Portal as a global administrator or another role that is able to manage this application.

**Step2**: Navigate to Azure Active Directory, and on the list of Enterprise applications, find the application for which you want to
           enable federated single sign-on.

**Step3**: Click on the application name to open it.Then, on the application's left-hand navigation menu, click "Single Sign-On".

**Step4**: Under Domain and URLs section, update or enter the Reply URL (ACS URL) in Azure AD with the correct value <!--$ReplyUrl-->ReplyUrl<!--/$ReplyUrl-->. If you don’t see a Reply URL field, pleaes check the "Show Advance URL settings" section.

Your application should now be available for user sign-in.

For more information on common application-related issues, please refer to the following document: <!--$AppSignInErrorHelpPage-->AppSignInErrorHelpPage<!--/$AppSignInErrorHelpPage-->