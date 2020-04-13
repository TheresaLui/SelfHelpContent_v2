<properties
	pageTitle="I have a problem with configuring ADFS in AADConnect"
	description="I have a problem with configuring ADFS in AADConnect"
	service="microsoft.activedirectory"
	resource="activedirectory"
	authors="rodejo"
	ms.author="rodejo"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32684514"
	resourceTags=""
	productPesIds="16666"
	cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	articleId="e7f2fa8f-4f36-497b-8f7d-4c76f37b7f12"
	ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# I have a problem with configuring ADFS in AADConnect

## **Recommended Steps**

Please review one of the below options to troubleshoot problems or to learn more about configuring ADFS in AADConnect:

* [I want to learn more about ADFS and Azure AD Connect](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectfed-whatis)
* [Users with alternate login ID (user principal name other than on-premises userPrincipalName attribute) are not able to authenticate](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-federation-management#federate-with-azure-ad-using-alternateid-a-namealternateida)
*  [I want to federate another domain with AD FS using AAD Connect](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-federation-management#add-a-federated-domain-a-nameaddfeddomaina)
*  I see an error "Requested federation realm object does not exist". This error is usually thrown by Azure AD when the issuerID claim issued given by AD FS is incorrect. In some of the older versions of Azure AD Connect the issuance claims in multiple domain federation scenarios were not set correctly. Upgrading to latest Azure AD Connect will likely resolve the issue.


## **Recommended Documents**

* [Azure AD Connect and Federation](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectfed-whatis)
<br>
