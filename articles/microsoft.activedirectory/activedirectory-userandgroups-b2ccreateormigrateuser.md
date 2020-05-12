 <properties
	pageTitle="Business to Consumer (B2C)/Creating or migrating users into B2C"
	description="Business to Consumer (B2C)/Creating or migrating users into B2C"
	service="microsoft.aad"
	resource="Microsoft_AAD_IAM"
	authors="parakhj"
	displayOrder="901"
	selfHelpType="resource"
	supportTopicIds="32416703"
	resourceTags="userandgroups_overview,userandgroups_user,userandgroups_group"
	productPesIds="14785,16580"
	cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	articleId="9c3caee9-a539-4c9d-afb9-9a713e01ab49"
	ownershipId="AzureIdentity_B2C"
/>

# B2C: How to create or migrate users into Azure AD B2C

The only way to create Azure AD B2C users that can sign in through your B2C integrated app is either:

* Having the user sign-up via a [sign-up](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-reference-policies#create-a-sign-up-policy) or [sign-up/sign-in](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-reference-policies#create-a-sign-up-or-sign-in-policy) policy
* Using the [Graph API](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-devquickstarts-graph-dotnet)

While it is possible to create users via the Azure Portal UI, those users will not be able to sign-in and properly use Azure AD B2C.

If you’d like to be able to create Azure AD B2C users via the portal, you can request this functionality in the [Azure AD B2C UserVoice](https://feedback.azure.com/forums/169401-azure-active-directory/category/160596-b2c) forum.

## **Recommended documents**

* [Graph API](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-devquickstarts-graph-dotnet)
* [Stack Overflow](http://stackoverflow.com/questions/tagged/azure-ad-b2c)
* [UserVoice](https://feedback.azure.com/forums/169401-azure-active-directory/category/160596-b2c)