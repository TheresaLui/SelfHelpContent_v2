<properties
    pageTitle="Enterprise Application - Config issue preventing user sign-in"
    description="Enterprise Application - Config issue preventing user sign-in"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="asbh"
    ms.author="asbh"
    displayOrder="1"
    articleId="Application_SignIn_ADSTS_50003"
    diagnosticScenario="EnterpriseApps"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>

# Configuration Issue Preventing User Sign-In

The certificate for your application is invalid or expired. Please activate the existing certificate, or create and apply a new one. An invalid certificate will prevent any user from accessing this application. 

In order to enable user sign-in for this application, please follow these steps:

1. Sign in to the [Azure Portal](https://portal.azure.com/) as a global administrator (or any role with permissions to manage this application)
2. Select **Azure Active Directory** and go the "Enterprise applications" blade. Search for the application for which you want to enable federated single sign-on.
3. Click on the application name to open it, then click "Single Sign-On" on the application's left-hand navigation menu
4. Click the "Create new certificate" button under the SAML signing Certificate section
5. Enter a valid expiration date and click Save
6. Select the checkbox to make the new certificate active, then click Save to replace the old certificate with the new one
7. Under "SAML Sign-in Certificate", click "Remove" to remove the unused certificate
8. Download the new active certificate and update it in your application

Your application should now be available for user sign-in.

For more information on common application-related issues, please refer to the following document: <!--$AppSignInErrorHelpPage-->AppSignInErrorHelpPage<!--/$AppSignInErrorHelpPage-->
