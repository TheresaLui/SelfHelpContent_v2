<properties
    pageTitle="Enterprise Application - Config issue preventing user sign-in"
    description="Enterprise Application - Config issue preventing user sign-in"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="luleon"
    ms.author="luleon"
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

## **Recommended Steps**

1. Sign in to the [Azure Portal](https://portal.azure.com/) as a global administrator (or any role with permissions to manage this application)
2. Select **Azure Active Directory** and go the **Enterprise applications** blade. Search for the application for which you want to enable federated single sign-on. If you do not see the application you need, use the Filter control at the top of the All Applications List and set the Show option to All applications
3. Click on the application name to open it, then click **Single sign-on** on the application's left-hand navigation menu
4. Click the pencil under **Basic SAML Configuration**, then enter <!--$IdentifierUrl-->IdentifierUrl<!--/$IdentifierUrl--> into the **Identifier (Entity ID)** field and click save 

Your application should now be available for user sign-in.

For future sign in problems with SAML based applications, we recommend using the [testing feature with the My Apps secure sign-in extension](https://docs.microsoft.com/azure/active-directory/develop/active-directory-saml-debugging) to get better and automatic self diagnosis and resolution steps.

## **Recommended Documents**

* [Problem SignIn gallery applications](https://docs.microsoft.com/azure/active-directory/application-sign-in-problem-federated-sso-gallery)
