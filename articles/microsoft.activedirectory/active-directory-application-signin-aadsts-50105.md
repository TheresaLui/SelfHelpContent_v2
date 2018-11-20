<properties
    pageTitle="Enterprise Application - Config issue preventing user sign-in"
    description="Enterprise Application - Config issue preventing user sign-in"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="asbh"
    displayOrder="1"
    articleId="Application_SignIn_ADSTS_50105"
	diagnosticScenario="EnterpriseApps"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>

# Enterprise Application - Config issue preventing user sign-in

The user who is trying to log in does not have permissions to access the application. There are two possible scenarios for this problem. The most common is that user hasn't been assigned to the application.

In order to enable user sign-in for this application, please follow the steps below:

**Step 1**: Sign in to the Azure Portal as a global administrator or another role that is able to manage this application.

**Step 2**: Select Azure Active Directory and go to the 'Enterprise applications' blade. Search for the application for which you want to enable federated single sign on.

**Step 3**: Click on the application name to open it. Then, on the application's left-hand navigation menu, click "Single Sign-On".

**Step 4**: In the 'Users and groups' section, click on Add user to assign the user to the application.

If you have already assigned the user to the application but the problem still continues then the problem is that the Azure AD is trying to log the user into another instance of the application. This can occur because the 'Issuer' value in the sign-in request (SAML request) matches the 'Identifier' configured for other instance of the application. Please follow the steps below to resolve the issue:

**Step 1**: Identify the value of the "Issuer" property in the SAML request from the application. Follow  the instructions in this document to obtain a SAML request: <!--$AppSAMLDebugDoc-->AppSAMLDebugDoc<!--/$AppSAMLDebugDoc-->

**Step 2**: Sign in to the Azure Portal as a global administrator or another role that is able to manage this application.

**Step 3**: Select Azure Active Directory and go to the 'Enterprise applications' blade. Search for the application for which you want to enable federated single sign-on.

**Step 4**: Click on the application name to open it. Then, on the application's left-hand navigation menu, click "Single Sign-On".

**Step 5**: In the 'Domain and URLs' section, find the property labeled 'Identifier (Entity ID)'.

**Step 6**: If the ‘Issuer’ value does not match the ‘Identifier (Entity ID)’ then update the ‘Identifier (Entity ID) value to match. 

If the ‘Issuer’ value matches the Identifier (Entity ID) then there are two options::
    **Option A**: Use the current application to enable single sign-on and assign the users or group to the application.
	**Option B**: Update the application to provide a different ‘Issuer’ value in the SAML request.  Use this new value as the ‘Identifier (Entity ID)’ to enable single sign-on with the application you were configuring at first.

Your application should now be available for user sign-in.

For future sign-in problems with SAML based applications, we recommend using the testing feature with the My Apps secure sign-in extension to get better and automatic self diagnosis and resolution steps. For more information see: <!--$AppSAMLDebugDoc-->AppSAMLDebugDoc<!--/$AppSAMLDebugDoc-->

For more information on common application-related issues, please refer to the following document: <!--$AppSignInErrorHelpPage-->AppSignInErrorHelpPage<!--/$AppSignInErrorHelpPage-->