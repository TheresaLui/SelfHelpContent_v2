<properties
    pageTitle="Enterprise Application - Config issue preventing user sign-in"
    description="Enterprise Application - Config issue preventing user sign-in"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="luleon"
    ms.author="luleon"
    displayOrder="1"
    articleId="Application_SignIn_ADSTS_65005"
    diagnosticScenario="EnterpriseApps"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>

# Configuration Issue Preventing User Sign-In
<!--issueDescription-->
The application you were trying to sign into does not exist in the Azure Active Directory. The application may not be configured properly in Azure AD, or the Issuer value that is coming in the sign-in request (SAML request) does not match the application Identifier.
<!--issueDescription-->

## **Recommended Steps**

1. Identify the value of the *Issuer* property in the SAML request from the application. Follow the instructions in this document to obtain a SAML request: <!--$AppSAMLDebugDoc-->AppSAMLDebugDoc<!--/$AppSAMLDebugDoc-->.
2. Sign in to the [Azure Portal](https://portal.azure.com/) as a global administrator (or any role with permissions to manage this application)
3. Select **Azure Active Directory** and go the **Enterprise applications** blade. Search for the application for which you want to enable federated single sign-on.
4. Click on the application name to open it, then click **Single sign-on** on the application's left-hand navigation menu. If you do not see the application you need, use the Filter control at the top of the All Applications List and set the Show option to *All applications*.
5. Within the **Basic SAML Configuration' section**, click the pencil to edit the value
6. Enter the Issuer value into the **Identifier (Entity ID)** property and click save  

Your application should now be available for user sign-in.

For future sign in problems with SAML based applications, we recommend using the [testing feature with the My Apps secure sign-in extension](https://docs.microsoft.com/azure/active-directory/develop/active-directory-saml-debugging) to get better and automatic self diagnosis and resolution steps.

## **Recommended Documents**

* [Problem SignIn gallery applications](https://docs.microsoft.com/azure/active-directory/application-sign-in-problem-federated-sso-gallery)
