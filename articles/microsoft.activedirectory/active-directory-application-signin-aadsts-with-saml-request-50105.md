<properties
    pageTitle="Enterprise Application - Config issue preventing user sign-in"
    description="Enterprise Application - Config issue preventing user sign-in"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="asbh"
    ms.author="asbh"
    displayOrder="1"
    articleId="Application_SignIn_ADSTS_With_SAML_Request_50105"
    diagnosticScenario="EnterpriseApps"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>

# Configuration Issue Preventing User Sign-In

The user who is trying to log in does not have permission to access the application. There are two possible reasons for this, with the most common scenario being that the user has not been assigned to the application.

In order to enable user sign-in for this application, please follow the steps below:

1. Sign in to the [Azure Portal](https://portal.azure.com/) as a global administrator (or any role with permissions to manage this application)
2. Select **Azure Active Directory** and go the "Enterprise applications" blade. Search for the application for which you want to enable federated single sign-on.
3. Click on the application name to open it, then click "Single Sign-On" on the application's left-hand navigation menu
4. In the "Users and groups" section, click on **Add User** to assign the user to the application

If you have already assigned the user to the application but the problem still continues, then the likely problem is Azure AD trying to log the user into another instance of the application. This can occur because the "Issuer" value in the sign-in request (SAML request) matches the "Identifier" configured for another instance of the application. Please follow the steps below to resolve the issue:

1. Refer to the SAML request provided at the end of this article under the title "SAML Request Received", and copy the value of the \"Issuer\" property value
2. Sign in to the [Azure Portal](https://portal.azure.com/) as a global administrator (or any role with permissions to manage this application)
3. Select **Azure Active Directory** and go the "Enterprise applications" blade
4. Click on the application name to open it, then click "Single Sign-On" on the application's left-hand navigation menu
5. In the "Domain and URLs" section, find the property labeled "Identifier (Entity ID)"
6. If the "Issuer" value does not match the "Identifier (Entity ID)", update the "Identifier (Entity ID)" value to match
 
If the "Issuer" value already matches the "Identifier (Entity ID)", there are two options:

* **Option A**: Use the current application to enable single sign-on and assign the users or group to the application
* **Option B**: Update the application to provide a different "Issuer" value in the SAML request, then use this new value as the "Identifier (Entity ID)" to enable single sign-on with the application you were first configuring
 
Your application should now be available for user sign-in.

For future sign-in problems with SAML based applications, we recommend using the testing feature with the My Apps secure sign-in extension to get better and automatic self diagnosis and resolution steps. For more information see: <!--$AppSAMLDebugDoc-->AppSAMLDebugDoc<!--/$AppSAMLDebugDoc-->

For more information on common application-related issues, please refer to the following document: <!--$AppSignInErrorHelpPage-->AppSignInErrorHelpPage<!--/$AppSignInErrorHelpPage-->

<h4>SAML Request Received:</h4>				
<!--$SAMLRequestFormat-->SAMLRequestFormat<!--/$SAMLRequestFormat-->	
