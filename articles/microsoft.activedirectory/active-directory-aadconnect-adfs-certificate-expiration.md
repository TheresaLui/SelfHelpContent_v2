<properties
	pageTitle="Help with AD FS SSL or Token Signing Certificates"
	description="AD FS certificate expiration and how to troubleshoot"
	service="microsoft.aad"
	resource="Microsoft_AAD_IAM"
	authors="billmath"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32615367"
	resourceTags=""
	productPesIds="16579"
	cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    ms.author="billmath"
	articleId="6e1e9736-c28a-445e-8e1c-2064f3ff9bc1"
	ownershipId="AzureIdentity_MultiFactorAuthentication"
/>


# Certificate Expiration

* Use our [AD FS Certificate Troubleshooting Guide](https://adfshelp.microsoft.com/TroubleshootingGuides/Workflow/3828f87c-72b4-4b99-bbcf-fdf74268874c). This workflow helps to provide guidance on how to deploy new certificates as well as troubleshoot problems with existing certificates. It covers both Active Directory Federation Service (AD FS) and Web Application Proxy (WAP) servers. 
* To update the SSL Certificate, visit the [documentation instructions](https://docs.microsoft.com/windows-server/identity/ad-fs/operations/manage-ssl-certificates-ad-fs-wap)
* For help configuring token-signing/token-decrypting certificates, view our [documentation](https://docs.microsoft.com/windows-server/identity/ad-fs/operations/configure-ts-td-certs-ad-fs)

If your certificate has expired, try the following steps:

* If you have Azure AD Connect, follow the instructions to update your certificate through the [AD Connect tool](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-fed-ssl-update)
* For general certificate issues, use our [Diagnostics Analyzer](https://adfshelp.microsoft.com/DiagnosticsAnalyzer/Analyze) which provides a list of potential issues to help troubleshoot

- If you are unable to run the Diagnostics Analyzer:<br>

	*  Make sure that the certificate is trusted, as SSL certs need to be trusted by the clients and token signing certificates need to be trusted by relying parties
	* Check the trust chain. Every certificate in the chain needs to be valid
	* Check the certificate expiration date
	* Check certificate revocation list (CRL) accessibility, making sure the CDP field is populated
	* Finally, check to make sure the certificate has not been revoked

## **Recommended Documents**

- [Certificate Troubleshooting](https://docs.microsoft.com/windows-server/identity/ad-fs/troubleshooting/ad-fs-tshoot-certs)<br>
- [Updating SSL Certificates](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-fed-ssl-update)<br>
- [AD FS Help](https://adfshelp.microsoft.com/)<br>
- [Azure AD Connect Health for AD FS](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-health-adfs)
