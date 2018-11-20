<properties
	pageTitle="Certificate Expiration"
	description="AD FS certificate expiration and how to troubleshoot"
	service="microsoft.aad"
	resource="Microsoft_AAD_IAM"
	authors="billmath"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32615367"
	resourceTags=""
	productPesIds="16579"
	cloudEnvironments="public"
/>


# Certificate Expiration




- If your certificate has expired, update your certificate through the [AD Connect tool](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-fed-ssl-update).<br>
- For general certificate issues, use our [Diagnostics Analyzer](https://adfshelp.microsoft.com/DiagnosticsAnalyzer/Analyze) which provides a list of potential issues to help troubleshoot.<br>
- If you are unable to run the Diagnostics Analyzer:<br>
    *  Make sure that the certificate is trusted, as SSL certs need to be trusted by the clients and token signing certificates need to be trusted by relying parties.<br>
    * Check the trust chain, every certificate in the chain needs to be valid.
    * Check the certificate expiration date.<br>
    * Check certificate revocation list (CRL) accessibility, making sure the CDP field is populated.<br>
    * Finally, check to make sure the certificate has not been revoked.<br>

## **Recommended Documents**


- [Certificate Troubleshooting](https://docs.microsoft.com/windows-server/identity/ad-fs/troubleshooting/ad-fs-tshoot-certs)<br>
- [Updating SSL Certificates](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-fed-ssl-update)<br>
- [AD FS Help](https://adfshelp.microsoft.com/)
