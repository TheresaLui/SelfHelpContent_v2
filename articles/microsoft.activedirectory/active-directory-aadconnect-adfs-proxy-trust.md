<properties
	pageTitle="Proxy Trust"
	description="Troubleshoot proxy trust issues for AD FS"
	service="microsoft.aad"
	resource="Microsoft_AAD_IAM"
	authors="billmath"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32615427"
	resourceTags=""
	productPesIds="16579"
	cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    ms.author="billmath"
	articleId="47d08123-bf64-42c0-9a1c-f1928b8115fb"
	ownershipId="AzureIdentity_MultiFactorAuthentication"
/>


# Troubleshoot Issues with the Web Application Proxy

### The proxy trust between Web Application Proxy (WAP) and Active Directory Federation Service (AD FS) server is broken

This [troubleshooting workflow](https://adfshelp.microsoft.com/TroubleshootingGuides/Workflow/da33a6cd-166b-4fca-863a-73aec904c3fd) helps to resolve issues with proxy trust configuration with AD FS. Use this workflow if you are seeing problems with your Web Application Proxy (WAP) trust configuration.

### I am seeing a large amount of 222 events

- Use the [Congestion Control troubleshooting guide](https://adfshelp.microsoft.com/TroubleshootingGuides/Workflow/c66ebfd4-8d70-40ce-ab56-86f559064b48) to troubleshoot this issue

### All users can't sign-in using AD FS from an external network

Use this [troubleshooting guide](https://adfshelp.microsoft.com/TroubleshootingGuides/Workflow/1183c7fd-7489-4957-a30c-ab497ee85657) if users are not able to authenticate using AD FS from outside corpnet. This would usually include authentications occurring via the Web Application Proxy (WAP).

### Other Issues

- Use our [Diagnostics Analyzer](https://adfshelp.microsoft.com/DiagnosticsAnalyzer/Analyze) to run a comprehensive health check on your AD FS server and help troubleshoot your issue

## **Recommended Documents**

- [General AD FS Help](https://adfshelp.microsoft.com/)<br>
- [Azure AD Connect Health for AD FS](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-health-adfs)
