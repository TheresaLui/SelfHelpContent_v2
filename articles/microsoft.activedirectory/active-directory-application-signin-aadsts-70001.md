<properties
    pageTitle="Application is not configured with the right Identifier URL"
    description="Application is not configured with the right Identifier URL"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="sridhara"
    displayOrder="1"
    articleId="Application_SignIn_AADSTS_70001"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>

# Application is not configured with the right Identifier URL

Please follow the steps below to resolve the issue

Step1: Sign-in into Azure portal as a Global administrator or another role that is able to manage this application.
Step2: Navigate to Azure Active Directory, and on the list of Enterprise applications, find the application to which you want to
       enable federated single sign on.
Step3: Click on the application name to open it. Then, on the application's left-hand navigation menu, click "Single sign-on".
Step4: Under Domain and URLs section, replace the current identifier value current identifier with <!--$IdentifierUrl-->[IdentifierUrl]<!--/$IdentifierUrl-->

Please refer to this doc for common Application related issues: <!--$AppSignInErrorHelpPage-->[AppSignInErrorHelpPage]<!--/$AppSignInErrorHelpPage-->