<properties
	pageTitle="Synchronizing AD to Azure AD/Azure AD Connect AD FS Configuration"
	description="Synchronizing AD to Azure AD/Azure AD Connect AD FS Configuration"
	service="microsoft.activedirectory"
	resource="activedirectory"
	authors="cychua"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32404463"
	resourceTags=""
	productPesIds="14785"
	cloudEnvironments="public"
/>

# I have trouble configuring / managing federation with AD FS

## **Recommended steps**
Azure AD Connect provides easy steps to configure and maintain federation. For all the federation related tasks with AAD Connect read [Azure AD Connect and federation](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectfed-whatis). Some of the common issues and solutions are listed below:

1. Users with alternate login ID (user principal name other than on-premises userPrincipalName attribute) are not able to authenticate.
The most common reason for failures in case of alternate login ID is wrong issuance claim rules. The latest version of Azure AD Connect helps configure federation with alternate login ID with the requisite configuration on AD FS farm. Read [more](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-federation-management#federate-with-azure-ad-using-alternateid-a-namealternateida).

2. How do I federate another domain with AD FS using AAD Connect?
You can use Add an additional Azure AD domain task in Azure AD Connect to federate multiple domain with your AD FS. Read [more](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-federation-management#add-a-federated-domain-a-nameaddfeddomaina).

3. Users are getting error “Requested federation realm object does not exist”.
This error is usually thrown by Azure AD when the issuerID claim issued given by AD FS is incorrect. In some of the older versions of Azure AD Connect the issuance claims in multiple domain federation scenarios were not set correctly. Upgrading to latest Azure AD Connect will likely resolve the issue.


## **Recommended documents**
[Azure AD Connect and Federation](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectfed-whatis)
<br>
