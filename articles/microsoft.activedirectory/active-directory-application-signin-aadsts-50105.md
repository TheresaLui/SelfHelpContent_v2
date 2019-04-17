<properties
    pageTitle="Enterprise Application - Config issue preventing user sign-in"
    description="Enterprise Application - Config issue preventing user sign-in"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="luleon"
    authoralias="luleon"
    displayOrder="1"
    articleId="Application_SignIn_ADSTS_50105"
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
2. Select **Azure Active Directory** and go the **Enterprise applications** blade. Search for the application for which you want to enable federated single sign-on
3. Click on the application name to open it, then click **Single Sign-On** on the application's left-hand navigation menu. If you do not see the application you want show up here, use the Filter control at the top of the All Applications List and set the Show option to **All applications**
4. Once the application loads, select **Users and Groups** from the application’s left-hand navigation menu.
5. In the **Users and groups** section, click on **Add** button on top of the Users and Groups list to open the Add Assignment pane
6. Select the **Users and groups** selector from the Add Assignment pane. In the *Search by name or email address* search box, type the full name or email address of the user that you want to add. Hover over the user in the list to reveal a checkbox. Click the checkbox next to the user’s profile photo or logo to add the user to the Selected list
7. When you're finished selecting users, click the Select button to add them to the list of users and groups to be assigned to the application
8. Click the **Assign** button to assign the application to the selected users.

If you have already assigned the user to the application but the problem still continues, then the likely problem is Azure AD trying to log the user into another instance of the application. This can occur because the "Issuer" value in the sign-in request (SAML request) matches the "Identifier" configured for other instance of the application. Please follow the steps below to resolve the issue:

1. Identify the value of the *Issuer* property in the SAML request from the application. Follow  the instructions in this document to obtain a SAML request: <!--$AppSAMLDebugDoc-->AppSAMLDebugDoc<!--/$AppSAMLDebugDoc-->
2. Sign in to the [Azure Portal](https://portal.azure.com/) as a global administrator (or any role with permissions to manage this application)
3. Select **Azure Active Directory** and go the **Enterprise applications** blade
4. Click on the application name to open it, then click **Single Sign-On** on the application's left-hand navigation menu
5. In the **Domain and URLs** section, find the property labeled **Identifier (Entity ID)**
6. If the **Issuer** value does not match the **Identifier (Entity ID)**, update the **Identifier (Entity ID)** value to match

If the *Issuer* value already matches the **Identifier (Entity ID)**, there are two options:

* **Option A**: Use the current application to enable single sign-on and assign the users or group to the application
* **Option B**: Update the application to provide a different "Issuer" value in the SAML request, then use this new value as the "Identifier (Entity ID)" to enable single sign-on with the application you were first configuring

Your application should now be available for user sign-in

For future sign in problems with SAML based applications, we recommend using the testing feature with the My Apps secure sign-in extension to get better and automatic self diagnosis and resolution steps. For more information see [this link](https://docs.microsoft.com/azure/active-directory/develop/active-directory-saml-debugging)

For more information on common application-related issues, please refer to the following document: [Problem SignIn gallery applications](https://docs.microsoft.com/azure/active-directory/application-sign-in-problem-federated-sso-gallery)
