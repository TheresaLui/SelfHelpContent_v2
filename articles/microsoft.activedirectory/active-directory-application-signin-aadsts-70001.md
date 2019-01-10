<properties
    pageTitle="Enterprise Application - Config issue preventing user sign-in"
    description="Enterprise Application - Config issue preventing user sign-in"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="sridhara"
    ms.author="sridhara"
    displayOrder="1"
    articleId="Application_SignIn_ADSTS_70001"
	diagnosticScenario="EnterpriseApps"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>

# Configuration Issue Preventing User Sign-In

Your <!--$AppDisplayName-->AppDisplayName<!--/$AppDisplayName--> is not configured with the right Identifier URL.

In order to enable user sign-in for this application, please follow the steps below:

1. Sign in to the [Azure Portal](https://portal.azure.com/) as a global administrator (or any role with permissions to manage this application)
2. Select **Azure Active Directory** and go the "Enterprise applications" blade. Search for the application for which you want to enable federated single sign-on.
3. Click on the application name to open it, then click "Properties" on the application's left-hand navigation menu
4. Click the pencil under "Basic SAML Configuration", then enter <!--$IdentifierUrl-->IdentifierUrl<!--/$IdentifierUrl--> into the "Identifier (Entity ID)" field and click save 

Your application should now be available for user sign-in.

For more information on common application-related issues, please refer to the following document: <!--$AppSignInErrorHelpPage-->AppSignInErrorHelpPage<!--/$AppSignInErrorHelpPage-->
