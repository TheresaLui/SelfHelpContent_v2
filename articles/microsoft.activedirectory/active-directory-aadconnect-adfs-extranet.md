<properties
    pageTitle="Problem with authentication ONLY from the extranet"
    description="Self Help content for authentication issues from the extranet"
	  service="microsoft.aad"
	  resource="Microsoft_AAD_IAM"
 	authors="zhvolosh"
    ms.author="zhvolosh"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32689919"
    resourceTags=""
	productPesIds="16579"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    	articleId="c0bae8c1-80c1-42ba-af0b-b4a5fffb8b9b"
	ownershipId="AzureIdentity_MultiFactorAuthentication"
/>

# Problem with authentication ONLY from the extranet

## **Recommended Steps**

### All users can't sign-in using AD FS from an external network

Use this [troubleshooting guide](https://adfshelp.microsoft.com/TroubleshootingGuides/Workflow/1183c7fd-7489-4957-a30c-ab497ee85657) if users are not able to authenticate using AD FS from outside corpnet. This would usually include authentications occurring via the Web Application Proxy (WAP).

### The proxy trust between Web Application Proxy (WAP) and Active Directory Federation Service (AD FS) server is broken

This [troubleshooting workflow](https://adfshelp.microsoft.com/TroubleshootingGuides/Workflow/da33a6cd-166b-4fca-863a-73aec904c3fd) helps to resolve issues with proxy trust configuration with AD FS. Use this workflow if you are seeing problems with your Web Application Proxy (WAP) trust configuration.

### Issues with authentication with Windows Integrated Authentication

1. For configuration help for browsers to use Windows Integrated Authentication with AD FS, see the [documentation](https://docs.microsoft.com/windows-server/identity/ad-fs/operations/configure-ad-fs-browser-wia)
2. View our [AD FS Troubleshooting - WIA Guide](https://docs.microsoft.com/windows-server/identity/ad-fs/troubleshooting/ad-fs-tshoot-iwa) to troubleshoot possible issues
3. If users are seeing unexpected NTLM or forms based authentication prompts, use this [workflow](https://adfshelp.microsoft.com/TroubleshootingGuides/Workflow/e4d46600-59a9-4202-8fe7-7436fd56c486) to troubleshoot such issues

### Configure Smart Card Authentication

View our [documentation](https://docs.microsoft.com/windows-server/identity/ad-fs/operations/configure-user-certificate-authentication) for assistance configuring certificate authentication.
