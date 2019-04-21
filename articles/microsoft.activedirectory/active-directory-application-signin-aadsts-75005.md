<properties
    pageTitle="Enterprise Application - Config issue preventing user sign-in"
    description="Enterprise Application - Config issue preventing user sign-in"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="asbh"
    ms.author="asbh"
    displayOrder="1"
    articleId="Application_SignIn_ADSTS_75005"
	diagnosticScenario="EnterpriseApps"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>

# Configuration Issue Preventing User Sign-In

The authentication/SAML request that you are sending is invalid or missing properties.

To resolve this issue, please follow the steps below:

1. Follow the instructions in <!--$AppSAMLDebugDoc-->AppSAMLDebugDoc<!--/$AppSAMLDebugDoc--> to capture the SAML request

2. Share the SAML request and Azure AD single sign-on SAML protocol requirements (<!--$AppSSOSAMLProtocolPage-->AppSSOSAMLProtocolPage<!--/$AppSSOSAMLProtocolPage-->) with the owner or developer of the application

Your application should be available for user sign-in once the authentication request contains the required fields.

For future sign-in problems with SAML based applications, we recommend using the testing feature with the My Apps secure sign-in extension to get better and automatic self diagnosis and resolution steps. For more information see: <!--$AppSAMLDebugDoc-->AppSAMLDebugDoc<!--/$AppSAMLDebugDoc-->

For more information on common application-related issues, please refer to the following document: <!--$AppSignInErrorHelpPage-->AppSignInErrorHelpPage<!--/$AppSignInErrorHelpPage-->
