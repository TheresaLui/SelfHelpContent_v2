<properties
    pageTitle="Enterprise Application - Config issue preventing user sign-in"
    description="Enterprise Application - Config issue preventing user sign-in"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="asbh"
    displayOrder="1"
    articleId="Application_SignIn_ADSTS_With_SAML_Request_75005"
    diagnosticScenario="EnterpriseApps"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>

# Enterprise Application - Config issue preventing user sign-in

User was not able to Sign-in as we were not able to process authentication/SAML request. The SAML request was invalid or it was missing properties.

In order to enable user sign-in for this application, please follow the steps below:

**Step1**: Please refer to the SAML request provided at the end.

**Step2**: Share the SAML request and Azure AD single sign-on SAML protocol requirements with the software vendor or developer of the application. SAML protocol requirements link <!--$AppSSOSAMLProtocolPage-->AppSSOSAMLProtocolPage<!--/$AppSSOSAMLProtocolPage-->.

Your application should be available for user sign-in once the authentication request contains the required fields.
			
For future sign-in problems with SAML based applications, we recommend using the testing feature with My Apps secure Sign-in Extension to get better and automatic self diagnosis and resolution steps. For more information see: <!--$AppSAMLDebugDoc-->AppSAMLDebugDoc<!--/$AppSAMLDebugDoc-->

For more information on common application-related issues, please refer to the following document: <!--$AppSignInErrorHelpPage-->AppSignInErrorHelpPage<!--/$AppSignInErrorHelpPage-->

<h4>SAML Request Recieved:</h4>				
<!--$SAMLRequestFormatted-->SAMLRequestFormatted<!--/$SAMLRequestFormatted-->	