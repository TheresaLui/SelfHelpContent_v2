<properties
    pageTitle="Enterprise Application - Config issue preventing user sign-in"
    description="Enterprise Application - Config issue preventing user sign-in"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="asbh"
    displayOrder="1"
    articleId="Application_SignIn_ADSTS_With_SAML_Request_50105"
    diagnosticScenario="EnterpriseApps"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>

# Enterprise Application - Config issue preventing user sign-in

The user who is trying to login doesnt have permissions to access the application. There are two possible scenarios for this problem. The most common is that user hasn't been assigned to the application.

In order to enable user sign-in for this application, please follow the steps below:

**Step1**: Sign in to Azure Portal as a global administrator or another role that is able to manage this application.

**Step2**: Navigate to the Azure Active Directory, and go to the Enterprise applications blade, search for the application for which you want to
           enable federated single sign-on.

**Step3**: Click on the application name to open it. Then, on the application's left-hand navigation menu, click "Single Sign-On".

**Step4**: In the Users and groups section, click on Add user to assign the user to the application.

If you have already assigned the user to the application but the problem continues. Azure AD is signing the user to another instance of the application. It happens because the 'Issuer' value in the sign-in request (SAML request) matches the 'Identifier' configured for other instance of the application. Please follow the steps below to resolve the issue:

**Step1**: Get the SAML request given at the end, and copy the value of the \"Issuer\" property value.

**Step2**: Signin to the Azure Portal as a global administrator or another role that is able to manage this application.

**Step3**: Navigate to Azure Active Directory, and go to the list of Enterprise applications blade, search for the application for which you want to
           enable federated single sign-on.

**Step4**: Click on the application name to open it. Then, on the application's left-hand navigation menu, click "Single Sign-On".

**Step5**: In the Domain and URLs section, find the property labeled 'Identifier (Entity ID)'. Please check if the 'Issuer' value matches the 'Identifier (Entity ID)' configured for that instance.

If it matches, you can do one of the below:
     **StepA**: Use the current application to enable single sign-on and assign the users or group to the application.
	 **StepB**: Update the configuration on the software vendor to provide a different identifier. Use this value as the 'Identifier (Entity ID)' to enable single sign-on with the application you were configuring at first.

Your application should now be available for user sign-in.

For future sign-in problems with SAML based applications, we recommend using the testing feature with My Apps secure Sign-in Extension to get better and automatic self diagnosis and resolution steps. For more information see: <!--$AppSAMLDebugDoc-->AppSAMLDebugDoc<!--/$AppSAMLDebugDoc-->

For more information on common application-related issues, please refer to the following document: <!--$AppSignInErrorHelpPage-->AppSignInErrorHelpPage<!--/$AppSignInErrorHelpPage-->

<h4>SAML Request Recieved:</h4>				
<!--$SAMLRequestFormat-->SAMLRequestFormat<!--/$SAMLRequestFormat-->	