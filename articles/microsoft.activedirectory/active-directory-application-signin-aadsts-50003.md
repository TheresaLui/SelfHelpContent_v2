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

Application certificate is not valid. New certificate should be created or the existing certificate should be made active. This will prevent any user from accessing this application.

In order to enable user sign-in for this application, please follow the steps below:

**Step1**: Sign-in to Azure Portal as a global administrator or another role that is able to manage this application.

**Step2**: Navigate to Azure Active Directory, and on the list of Enterprise applications, find the application for which you want to
           enable federated single sign-on.

**Step3**: Click on the application name to open it.Then, on the application's left-hand navigation menu, click "Single Sign-On".

**Step4**: Click Create new certificate under the SAML signing Certificate section. Select Expiration date. Click Save.

**Step5**: Select the checkbox and make new certificate active to replace the old certificate. Then please click Save at the top of the pane and accept to activate the rollover certificate..

**Step6**: Under the SAML Sign-in Certificate section, click Remove to remove the Unused certificate.

**Step7**: Download the new active certificate and update it in the software vendor application.

Your application should now be available for user sign-in.

For more information on common application-related issues, please refer to the following document: <!--$AppSignInErrorHelpPage-->AppSignInErrorHelpPage<!--/$AppSignInErrorHelpPage-->