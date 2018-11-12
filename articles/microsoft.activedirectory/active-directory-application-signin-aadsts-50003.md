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

The certificate for you application is not valid or is either expired. A new certificate should be created or the existing certificate should be made active. An Invalid certificate will prevent any user from accessing this application.

In order to enable user sign-in for this application, please follow the steps below:

**Step1**: Sign in to the Azure Portal as a global administrator or another role that is able to manage this application.

**Step2**: Navigate to the Azure Active Directory, and on the list of Enterprise applications blade, search the application for which you want to
           enable federated single sign-on.

**Step3**: Click on the application name to open it. Then, on the application's left-hand navigation menu, click "Single Sign-On".

**Step4**: Click on "Create new certificate" button under the SAML signing Certificate section. Select the expiration date and finally, click Save.

**Step5**: Select the checkbox and make new certificate active to replace the old certificate. Then please click Save at the top of the pane and this will make your new certificate active.

**Step6**: Under the SAML Sign-in Certificate section, click Remove to remove the unused certificate.

**Step7**: Download the new active certificate and update it in your application.

Your application should now be available for user sign-in.

For more information on common application-related issues, please refer to the following document: <!--$AppSignInErrorHelpPage-->AppSignInErrorHelpPage<!--/$AppSignInErrorHelpPage-->