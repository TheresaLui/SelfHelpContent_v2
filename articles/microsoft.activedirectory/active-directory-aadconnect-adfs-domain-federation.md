<properties
	pageTitle="Domain federation with Azure AD"
	description="Troubleshoot domain federation with AD FS and Azure AD"
	service="microsoft.aad"
	resource="Microsoft_AAD_IAM"
	authors="billmath"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32615375"
	resourceTags=""
	productPesIds="16579"
	cloudEnvironments="public"
/>


# Domain Federation with Azure Active Directory

## **Recommended Steps**
1. For domain federation with AD Connect, troubleshoot using the documentation [here](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-fed-management).<br>
2. If not, use powershell for federation.<br>
    * Connect to Microsoft Online Services with the credential variable set previously<br>
    `Connect-MsolService –Credential $cred`<br>
    * Set the MSOL ADFS Context server, to the ADFS server
    `Set-MsolADFSContext –Computer adfs_servername.domain_name.com`<br>
    * Convert the domain to a federated domain
   ` Convert-MsolDomainToFederated –DomainName domain_name.com`<br>
    * Successful Federation
    `Successfully updated ‘domain_name.com‘ domain.`<br>
    * Verify federation
    `Get-MsolFederationProperty –DomainName domain_name.com`<br>

3. For new claims, utilize the [ADFS RPT Claims Tool](https://adfshelp.microsoft.com/AadTrustClaims/ClaimsGenerator).<br>

## **Recommended Documents**
[Troubleshooting ADFS with Azure AD](https://docs.microsoft.com/windows-server/identity/ad-fs/troubleshooting/ad-fs-tshoot-azure)<br>
[ADFS RPT Claims Tool](https://adfshelp.microsoft.com/AadTrustClaims/ClaimsGenerator)<br>
[ADFS Help](https://adfshelp.microsoft.com/)<br>
[AD Connect Information](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-fed-management)