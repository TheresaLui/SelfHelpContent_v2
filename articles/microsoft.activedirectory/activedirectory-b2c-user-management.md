 <properties
	pageTitle="Business to Consumer (B2C)"
	description="Business to Consumer (B2C)"
	service="microsoft.azureactivedirectory"
	resource="b2cDirectories"
	authors="parakhj"
	ms.author="parja"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32633306,32633307,32633315,32633319,32633322"
	resourceTags=""
	productPesIds="16580"
	cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	articleId="4ae814d3-0dc5-4987-b830-ec784cc61b03"
	ownershipId="AzureIdentity_B2C"
/>

# Business to Consumer (B2C)

## **Recommended Steps**

### **Creating or migrating users into Azure AD B2C**

The only way to create Azure AD B2C users that can sign in through your B2C integrated app is either:

* Having the user sign-up via a [sign-up](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-reference-policies#create-a-sign-up-policy) or [sign-up/sign-in](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-reference-policies#create-a-sign-up-or-sign-in-policy) policy
* Using the [Graph API](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-devquickstarts-graph-dotnet)

While it is possible to create users via the Azure Portal UI, those users will not be able to sign-in and properly use Azure AD B2C.

If you’d like to be able to create Azure AD B2C users via the portal, you can request this functionality in the [Azure AD B2C UserVoice](https://feedback.azure.com/forums/169401-azure-active-directory/category/160596-b2c) forum.

## **Recommended Documents**

* [Frequently asked questions](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-faqs)
* [Stackoverflow](http://stackoverflow.com/questions/tagged/azure-ad-b2c)
* [UserVoice](https://feedback.azure.com/forums/169401-azure-active-directory/category/160596-b2c)
