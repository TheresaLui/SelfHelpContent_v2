<properties
	pageTitle="I configured the app in my tenant with the permissions it needs, but I still get a 401 unauthorized error when trying to use it"
	description="I configured the app in my tenant with the permissions it needs, but I still get a 401 unauthorized error when trying to use it"
	service="microsoft.aad"
	resource="Microsoft_AAD_IAM"
	authors="PatAltimore"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32134056"
	resourceTags=""
	productPesIds="14785"
	cloudEnvironments="public"
/>

# I configured the app in my tenant with the permissions it needs, but I still get a 401 unauthorized error when trying to use it

## **Recommended steps**

1. On your web client application’s configuration page in the Azure portal, set the permissions your application requires by using the menus in the **Required Permissions** section.<br>
2. When the app authenticates to Azure AD if consent has not already been granted, Azure AD will prompt the user for consent and will display the required permissions it needs to function.
3. Administrators can consent to an application's delegated permissions on behalf of all the users in the tenant. An administrator can do this from the Azure portal. From the **Settings** blade for the application, click **Required Permissions** and click on the **Grant Permissions** button. <br>
[Overview of the consent framework](https://docs.microsoft.com/en-us/azure/active-directory/develop/active-directory-integrating-applications#overview-of-the-consent-framework)

## **Recommended documents**
[Integrating applications with Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/develop/active-directory-integrating-applications)