<properties
	pageTitle="Claim Rule Configuration"
	description="Configure claim rules and how to troubleshoot them for AD FS"
	service="microsoft.aad"
	resource="Microsoft_AAD_IAM"
	authors="billmath"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32615368"
	resourceTags=""
	productPesIds="16579"
	cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    ms.author="billmath"
	articleId="e5a77324-fcfe-46c1-9bc0-c4c21d423fc7"
	ownershipId="AzureIdentity_MultiFactorAuthentication"
/>

# Claim Rule Configuration

To resolve claim rule issues, try the following steps:

- Use the [Claims X-ray](https://adfshelp.microsoft.com/ClaimsXray/TokenRequest) service within  [AD FS Help](https://adfshelp.microsoft.com/) to debug and troubleshoot problems with claims issuance
- Ensure you have the right claims for your federation trust between Azure AD and AD FS with our [online claims generation tool](https://adfshelp.microsoft.com/AadTrustClaims/ClaimsGenerator)
- For additional troubleshooting for the claims issuance process, use [Fiddler](https://docs.microsoft.com/windows-server/identity/ad-fs/troubleshooting/ad-fs-tshoot-fiddler)

## **Recommended Documents**

- [Troubleshooting Claims Syntax](https://docs.microsoft.com/windows-server/identity/ad-fs/troubleshooting/ad-fs-tshoot-claims-rules)<br>
- [Claims X-ray](https://adfshelp.microsoft.com/ClaimsXray/TokenRequest)<br>
- [AD FS Help](https://adfshelp.microsoft.com/)<br>
- [Azure AD Connect Health for AD FS](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-health-adfs)
