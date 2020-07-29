<properties
	pageTitle="Check if domain controller is discoverable"
	description="Check if domain controller is discoverable"
	service="microsoft.identity"
	resource=""
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="62ebbe6a-9153-41e7-b3d6-d4f9a7fb2415"
/>

# How to check if domain controller is discoverable

* Azure AD Connect includes a powershell module to detect local DNS issues
* Example syntax is below

~~~powershell

Confirm-DnsConnectivity [-Forest] <String> [-DCs] <Array> [-ReturnResultAsPSObject] [<CommonParameters>]
ex:
Confirm-DnsConnectivity -Forest "TEST.CONTOSO.COM" -DCs "MYDC1.CONTOSO.COM","MYDC2.CONTOSO.COM"

~~~

## **Recommended Documents**

* [Use Azure AD Connect ADConnectivityTools PowerShell to check AD connectivity](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/reference-connect-adconnectivitytools)
