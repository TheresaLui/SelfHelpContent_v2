<properties
	pageTitle="Unable to read ToU on signin"
	description="End users unable to read the terms of use documents while signing in"
	service="microsoft.aad"
	resource="Microsoft_AAD_IAM"
	authors="IdentityMy"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32596870"
	resourceTags=""
	productPesIds="16577"
	cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	articleId="751899d0-99c0-43d2-b03b-78996e99d80e"
	ownershipId="AzureIdentity_ComplianceAndReporting"
/>

# End users can't read terms of use documents at sign-in

When an end user is signing into an application and a conditional access policy requires a terms of use, that end user will be required to accept prior to getting access. Depending on the font size within the terms of use PDF it may appear as blurry to end users on mobile devices.

## **Recommended steps**


1. Update the text within the terms of use PDF to font size of 24 pt (this is the recommended font size).
2. Create a new terms of use using that new PDF.
3. Update the CA policy to use the new terms of use with 24 pt font size.


## **Recommended documents**
* [Terms of Use Documentation](https://docs.microsoft.com/azure/active-directory/governance/active-directory-tou#terms-of-use-document)
