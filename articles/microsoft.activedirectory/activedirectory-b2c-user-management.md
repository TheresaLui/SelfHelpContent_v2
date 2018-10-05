 <properties
	pageTitle="Business to Consumer (B2C)"
	description="Business to Consumer (B2C)"
	service="microsoft.azureactivedirectory"
	resource="b2cDirectories"
	authors="parakhj"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32570972"
	resourceTags=""
	productPesIds="14785,16580"
	cloudEnvironments="public"
/>

# Business to Consumer (B2C)

## **Recommended steps**

### **Creating or migrating users into Azure AD B2C**

The only way to create Azure AD B2C users that can sign in through your B2C integrated app is either:

* Having the user sign-up via a [sign-up](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-reference-policies#create-a-sign-up-policy) or [sign-up/sign-in](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-reference-policies#create-a-sign-up-or-sign-in-policy) policy
* Using the [Graph API](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-devquickstarts-graph-dotnet)


While it is possible to create users via the Azure Portal UI, those users will not be able to sign-in and properly use Azure AD B2C.

If you’d like to be able to create Azure AD B2C users via the portal, you can request this functionality in the [Azure AD B2C UserVoice](https://feedback.azure.com/forums/169401-azure-active-directory/category/160596-b2c) forum.


## **Recommended documents**

* [Frequently asked questions](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-faqs)
* [Stackoverflow](http://stackoverflow.com/questions/tagged/azure-ad-b2c)
* [UserVoice](https://feedback.azure.com/forums/169401-azure-active-directory/category/160596-b2c)