<properties
    pageTitle="Enterprise Application - Config issue preventing user sign-in"
    description="Enterprise Application - Config issue preventing user sign-in"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="sridhara"
    displayOrder="1"
    articleId="Application_SignIn_ADSTS_70001"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>

# Enterprise Application - Config issue preventing user sign-in

<!--$AppDisplayName-->AppDisplayName<!--/$AppDisplayName--> is not enabled for user sign-in. This will prevent any user from accessing this application.

In order to enable user sign-in for this application, please follow the steps below:

**Step1**: Sign-in to Azure Portal as a global administrator or another role that is able to manage this application.

**Step2**: Navigate to Azure Active Directory, and on the list of Enterprise applications, find the application for which you want to
           enable federated single sign-on.

**Step3**: Click on the application name to open it. Then, on the application's left-hand navigation menu, click "Properties".

**Step4**: Set the value of the "Enabled for user to sign-in" property to "Yes".

Your application should now be available for user sign-in.

For more information on common application-related issues, please refer to the following document: <!--$AppSignInErrorHelpPage-->AppSignInErrorHelpPage<!--/$AppSignInErrorHelpPage-->