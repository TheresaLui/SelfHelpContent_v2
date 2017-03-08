 <properties
	pageTitle="Business to Consumer (B2C)/Creating or migrating users into B2C"
	description="Business to Consumer (B2C)/Creating or migrating users into B2C"
	service="microsoft.activedirectory"
	resource="activedirectory"
	authors="parakhj"
	displayOrder=""
	selfHelpType="resource"
	supportTopicIds="32416703"
	resourceTags=""
	productPesIds="14785"
	cloudEnvironments="public"
/>

# How to create or migrate users into Azure AD B2C

The only way to create Azure AD B2C users that can sign in through your B2C integrated app is either:

* Having the user sign-up via a [sign-up](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-reference-policies#create-a-sign-up-policy) or [sign-up/sign-in](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-reference-policies#create-a-sign-up-or-sign-in-policy) policy
* Using the [Graph API](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-devquickstarts-graph-dotnet)


While it is possible to create users via the Azure Portal UI, those users will not be able to sign-in and properly use Azure AD B2C.

If you’d like to be able to create Azure AD B2C users via the portal, you can request this functionality in the [Azure AD B2C UserVoice](https://feedback.azure.com/forums/169401-azure-active-directory/category/160596-b2c) forum.


## **Recommended documents**
[Azure AD B2C Policies](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-reference-policies)
<br>
[Graph API](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-devquickstarts-graph-dotnet)
<br>
[UserVoice](https://feedback.azure.com/forums/169401-azure-active-directory/category/160596-b2c)