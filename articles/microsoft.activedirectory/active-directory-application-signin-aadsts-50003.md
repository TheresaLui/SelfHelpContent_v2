<properties
    pageTitle="Enterprise Application - Config issue preventing user sign-in"
    description="Enterprise Application - Config issue preventing user sign-in"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="luleon"
    ms.author="luleon"
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
2. Select **Azure Active Directory** and go the **Enterprise applications** blade. Search for the application for which you want to enable federated single sign-on.
3. Click on the application name to open it, then click **Single Sign-On** on the application's left-hand navigation menu.If you do not see the application you want show up here, use the Filter control at the top of the All applications List and set the Show option to *All applications*.
4. Click the **Create new certificate** button under the **SAML signing Certificate** section
5. Select an expiration date and click Save
6. Select the checkbox to make the new certificate active, then click Save to replace the old certificate with the new one
7. Check **Make new certificate** active to override the active certificate. Then, click **Save** at the top of the pane and accept to activate the rollover certificate.
8. Under the **SAML Signing Certificate** section, click remove to remove the Unused certificate.

Your application should now be available for user sign-in.

For future sign in problems with SAML based applications, we recommend using the testing feature with the My Apps secure sign-in extension to get better and automatic self diagnosis and resolution steps. For more information see [this link](https://docs.microsoft.com/azure/active-directory/develop/active-directory-saml-debugging)

For more information on common application-related issues, please refer to the following document: [Problem SignIn gallery applications](https://docs.microsoft.com/azure/active-directory/application-sign-in-problem-federated-sso-gallery)
