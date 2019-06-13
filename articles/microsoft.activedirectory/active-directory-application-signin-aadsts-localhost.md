<properties
    pageTitle="Enterprise Application - Config issue preventing user sign-in"
    description="Enterprise Application - Config issue preventing user sign-in"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="luleon"
    ms.author="luleon"
    displayOrder="1"
    articleId="Application_SignIn_ADSTS_Localhost"
	diagnosticScenario="EnterpriseApps"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>

# Configuration Issue Preventing User Sign-In
<!--issueDescription-->
Please delete the unused reply URL 127.0.0.1:444 configured for the application.
<!--issueDescription-->


## **Recommended Steps**

When the application was added as a non-gallery app, Azure Active Directory created https://127.0.0.1:444 reply URL as a default value. Please follow the steps below to delete this URL.

1. Sign in to the [Azure Portal](https://portal.azure.com/) as a global administrator (or any role with permissions to manage this application)
2. Select **Azure Active Directory** and go the **Enterprise applications** blade.
3. Select All Applications to view a list of all your applications. If you do not see the application you need, use the Filter control at the top of the All Applications List and set the Show option to *All applications*.
4. Select the application you want to configure for single sign-on
5. Once the application loads, open **Basic SAML configuration**. In the **Reply URL** (Assertion Consumer Service URL), delete unused or default Reply URLs created by the system, such as https://127.0.0.1:444/applications/default.aspx.

Your application should now be available for user sign-in.

For future sign in problems with SAML based applications, we recommend using the [testing feature with the My Apps secure sign-in extension](https://docs.microsoft.com/azure/active-directory/develop/active-directory-saml-debugging) to get better and automatic self diagnosis and resolution steps.

## **Recommended Documents**

* [Problem SignIn gallery applications](https://docs.microsoft.com/azure/active-directory/application-sign-in-problem-federated-sso-gallery)
