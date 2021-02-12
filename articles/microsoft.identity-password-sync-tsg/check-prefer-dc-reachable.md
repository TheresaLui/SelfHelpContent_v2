<properties
	pageTitle="Check if the preferred domain controller is reachable"
	description="Check if the preferred domain controller is reachable"
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
	articleId="ec41b322-4c33-4bdf-9e9b-1ea81c5045f4"
	   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# How to check if the preferred domain controller is reachable

1. Check what is/are the preferred DC(s) from the Synchronization Service Manager by going to the AD DS Connector properties and Configure Directory Partitions menu item
2. Confirm if the option to ‘Only use preferred domain controllers’ is enabled and click in ‘Configure….’ to see if there’s any preferred DCs configured
3. Then use Azure AD Connect ADConnectivityTools PowerShell to check connectivity against the Preferred DC

~~~powershell

Confirm-DnsConnectivity [-Forest] <String> [-DCs] <Array> [-ReturnResultAsPSObject] [<CommonParameters>]
ex:
Confirm-DnsConnectivity -Forest "TEST.CONTOSO.COM" -DCs "MYDC1.CONTOSO.COM","MYDC2.CONTOSO.COM"

~~~

## Recommended Documents

1. [Azure AD Connectivity Tools](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/reference-connect-adconnectivitytools)
