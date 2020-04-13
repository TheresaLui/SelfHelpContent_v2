<properties
	pageTitle="MFA Server (On-Premises)/Installing or configuring AD FS adapter"
	description="MFA Server (On-Premises)/Installing or configuring AD FS adapter"
	service="microsoft.aad"
	resource="Microsoft_AAD_IAM"
	authors="kgremban"
	displayOrder="230"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="mfa_overview"
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="b956c26d-4894-40cd-ac93-68174fc85667"
	ownershipId="AzureIdentity_User"
/>

# Help installing the AD FS adapter for Azure MFA Server

## **Recommended steps**

If you installed Azure Multi-Factor Authentication Server on the same server as ADFS, then you don't need the adapter. If you installed MFA Server on a different computer, use these steps when you install the ADFS adapter:

1.	Install the ADFS adapter on all ADFS servers. 
2.	If you're installing the adapter on multiple servers, only register it on the primary ADFS server (use the PowerShell script in the documentation). Restart all the ADFS servers for the registration to take effect. 
3.	Make sure the Web Services SDK is installed on the MFA server. Web service SDK is an IIS component. IIS needs to be installed prior to installing the Web service SDK. 
4.	If you have issue installing the ADFS adapter, make sure that the KB2919355 and .Net framework 4.x are installed. 
5.	The MSI installer of ADFS adapter is found under <C:\Program files\Multi-Factor Authentication server>. The file name is MultifactorAuthenticationAdfsAdapterSetup64.msi. 
6.	Check the version of ADFS OS. The adapter is available for Windows server 2012 R2 and later. For the earlier OS, you need to install the MFA server on ADFS box and integrate MFA with IIS authentication. 


## **Recommended documents**
- [Configure Azure Multi-Factor Authentication Server to work with AD FS in Windows Server 2012 R2](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started-adfs-w2k12)  
- [Configure Azure Multi-Factor Authentication Server to work with AD FS 2.0](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started-adfs-adfs2)  
- [Upgrade AD FS Adapter for MFA Server](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-server-upgrade#upgrade-the-ad-fs-adapters) 

