<properties
	pageTitle="I have AD FS installed and want to create federation with Azure Active Directory using PowerShell"
	description="Using PowerShell to create federation with Azure AD"
	service="microsoft.aad"
	resource="Microsoft_AAD_IAM"
	authors="billmath"
	displayOrder="3"
	selfHelpType="generic"
	supportTopicIds="32570968"
	resourceTags=""
	productPesIds="14785"
	cloudEnvironments="public"
/>



# I have AD FS installed and want to create federation with Azure Active Directory using PowerShell 

## **Recommended steps**

It is recommended to use Azure Active Directory Connect (Azure AD Connect) to establish federation between Azure AD and AD FS. Azure AD Connect can perform all the federation related tasks automatically. You can read more about the possible operations here. In case creating federation trust with AD FS is not possible using Azure AD Connect, the you can use PowerShell to create the federation trust with Azure AD.
Pre-requisite 

### Follow the guidelines here and install Azure PowerShell on AD FS server. 
Steps to create federation



1. Identify the set of domains you want to federate with Azure AD. While creating federation it is important to know if you are going to federate multiple domain with same AD FS
2. Run Microsoft Azure Active Directory PowerShell as administrator
3. Connect to Microsoft Online Services using GA credentials: `Convert-MsolService`
4. Set the MSOL AD FS Context server, to the AD FS server (optional): If you are not running the PowerShell module on the primary AD FS server, then set the right AD FS primary server as the context server:  `Set-MsolADFSConect -Computer <adfs_server.contoso.com>`
5. Now you can convert the domain(s) from managed to federated. If only one domain is to be federated, then the SupportMultipleDomain flag needs to be set as false while creating the trust, otherwise it needs to be set as true:  `Convert-MsoldomainToFederated -DomainName contoso.com -SupportMultipleDomain <$false/$true>`