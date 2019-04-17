<properties
    pageTitle="Enterprise Application - Config issue preventing user sign-in"
    description="Enterprise Application - Config issue preventing user sign-in"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="luleon"
    authoralias="luleon"
    displayOrder="1"
    articleId="Application_SignIn_ADSTS_50011"
    diagnosticScenario="EnterpriseApps"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>

# Configuration issue preventing user sign-in

The Authentication request (SAML request) that you are sending does not have the correct reply URL. This will prevent any user from accessing this application.

In order to enable user sign-in for this application, please follow the steps below:

1. Sign in to the [Azure Portal](https://portal.azure.com/) as a global administrator (or any role with permissions to manage this application)
2. Select **Azure Active Directory** and go the **Enterprise applications** blade. Search for the application for which you want to enable federated single sign-on.
3. Click on the application name to open it, then click **Single Sign-On** in the application's left-hand navigation menu. If you do not see the application you want show up here, use the Filter control at the top of the All Applications List and set the Show option to **All applications**
4. Within the **Basic SAML Configuration**, click the edit pencil and update or enter the appropriate Reply URL (Assertion Consumer Service URL), then click Save

Your application should now be available for user sign-in

For future sign in problems with SAML based applications, we recommend using the testing feature with the My Apps secure sign-in extension to get better and automatic self diagnosis and resolution steps. For more information see [this link](https://docs.microsoft.com/azure/active-directory/develop/active-directory-saml-debugging)

For more information on common application-related issues, please refer to the following document: [Problem SignIn gallery applications](https://docs.microsoft.com/azure/active-directory/application-sign-in-problem-federated-sso-gallery)
