<properties
    pageTitle="Enterprise Application - Config issue preventing user sign-in"
    description="Enterprise Application - Config issue preventing user sign-in"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="asbh"
    displayOrder="1"
    articleId="Application_SignIn_ADSTS_70001"
    diagnosticScenario="EnterpriseApps"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>

# Enterprise Application - Config issue preventing user sign-in

<!--$AppDisplayName-->AppDisplayName<!--/$AppDisplayName--> is not configured with the right Identifier URL. This will prevent any user from accessing this application.

In order to enable user sign-in for this application, please follow the steps below:

**Step1**: Sign-in to Azure Portal as a global administrator or another role that is able to manage this application.

**Step2**: Navigate to Azure Active Directory, and on the list of Enterprise applications, find the application for which you want to
           enable federated single sign-on.

**Step3**: Click on the application name to open it.Then, on the application's left-hand navigation menu, click "Single Sign-On".

**Step4**:  Under Domain and URLs section, replace the current identifier value current identifier with <!--$IdentifierUrl-->IdentifierUrl<!--/$IdentifierUrl-->.

Your application should now be available for user sign-in.

For more information on common application-related issues, please refer to the following document: <!--$AppSignInErrorHelpPage-->AppSignInErrorHelpPage<!--/$AppSignInErrorHelpPage-->