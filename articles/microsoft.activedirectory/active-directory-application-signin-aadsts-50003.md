<properties
    pageTitle="Enterprise Application - Config issue preventing user sign-in"
    description="Enterprise Application - Config issue preventing user sign-in"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="asbh"
    displayOrder="1"
    articleId="Application_SignIn_ADSTS_50003"
    diagnosticScenario="EnterpriseApps"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>

# Enterprise Application - Config issue preventing user sign-in

The certificate for your application is  invalid or  expired. A new certificate should be created or the existing certificate should be made active. An Invalid certificate will prevent any user from accessing this application.

In order to enable user sign-in for this application, please follow the steps below:

**Step 1**: Sign in to the Azure Portal as a global administrator or another role that is able to manage this application.

**Step 2**: Navigate to the Azure Active Directory and go the Enterprise applications blade, search for the application for which you want to enable federated single sign-on.

**Step 3**: Click on the application name to open it. Then, on the application's left-hand navigation menu, click "Single Sign-On".

**Step 4**: Click on the "Create new certificate" button under the SAML signing Certificate section. Select the expiration date and click Save.

**Step 5**: Select the checkbox to make the new certificate active and then click Save to replace the old certificate with this new one.

**Step 6**: Under the SAML Sign-in Certificate section, click Remove to remove the unused certificate.

**Step 7**: Download the new active certificate and update it in your application.

Your application should now be available for user sign-in.

For more information on common application-related issues, please refer to the following document: <!--$AppSignInErrorHelpPage-->AppSignInErrorHelpPage<!--/$AppSignInErrorHelpPage-->