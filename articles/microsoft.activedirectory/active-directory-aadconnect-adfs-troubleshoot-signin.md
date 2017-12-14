<properties
	pageTitle="I have configured federation with Azure AD using AD FS but sign-in is failing"
	description="Sign in is failing with Azure AD federation"
	service="microsoft.aad"
	resource="Microsoft_AAD_IAM"
	authors="billmath"
	displayOrder="1"
	selfHelpType="generic"
	supportTopicIds="32570971"
	resourceTags=""
	productPesIds="14785"
	cloudEnvironments="public"
/>

# I have configured federation with Azure AD using AD FS but sign-in is failing

## **Recommended steps**

Use [AD FS Help Troubleshooting Guides](https://aka.ms/adfshelp/troubleshooting) to quickly diagnose and resolve sign-in issues in AD FS. If you do not find a solution on AD FS Help, you may find the following resources helpful for an immediate resolution:

1.	**Troubleshoot generic AD FS service / sign-in issues:** Use [AD FS Diagnostic module from AD FS Help](https://adfshelp.microsoft.com/Tools/DownloadableTools) to diagnose the AD FS server issues.
2.	**Claims issuance related issues:** Use Claims X-Ray to debug claims issuance related issues. You can easily verify the final claims in a token using [Claims X-Ray](https://aka.ms/claimsxray)
3.	**Issues with SSL certificate update:** Use [Azure AD Connect to update the SSL certificate](https://aka.ms/adfssslwithaadconnect) of your AD FS farm. For detailed steps and guidance refer to [Managing SSL Certificates in AD FS and WAP in Windows Server 2016](https://docs.microsoft.com/windows-server/identity/ad-fs/operations/manage-ssl-certificates-ad-fs-wap)
4.	**Federation management with Azure AD Connect:** [Azure AD Connect](https://aka.ms/adfswithaadconnect) can help configure your federation trust with Azure AD correctly and resolve sign-in issues with Azure AD in a few simple clicks.

