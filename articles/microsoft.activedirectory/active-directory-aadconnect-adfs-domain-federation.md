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
	cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	ms.author="billmath"
	articleId="a203f2aa-c934-419c-8b06-9af9471197f8"
	ownershipId="AzureIdentity_MultiFactorAuthentication"
/>


# Domain Federation with Azure Active Directory

To resolve issues with domain federation, try the following steps:

- For domain federation with AD Connect, review the [troubleshooting documentation](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-fed-management)

- For other domain federation issues, use powershell for the following:
    1. Connect to Microsoft Online Services with the credential variable set previously<br>
    `Connect-MsolService –Credential $cred`<br>
    2. Set the MSOL ADFS Context server to the ADFS server<br>
    `Set-MsolADFSContext –Computer adfs_servername.domain_name.com`<br>
    3. Convert the domain to a federated domain<BR>
   ` Convert-MsolDomainToFederated –DomainName domain_name.com`<br>
    4. If it is successful, you will see `Successfully updated ‘domain_name.com‘ domain.`<br>
    5. Verify federation<BR>
    `Get-MsolFederationProperty –DomainName domain_name.com`<br>

- For new claims, use the [ADFS RPT Claims Tool](https://adfshelp.microsoft.com/AadTrustClaims/ClaimsGenerator)

## **Recommended Documents**


- [Troubleshooting AD FS with Azure AD](https://docs.microsoft.com/windows-server/identity/ad-fs/troubleshooting/ad-fs-tshoot-azure)<br>
- [AD FS RPT Claims Tool](https://adfshelp.microsoft.com/AadTrustClaims/ClaimsGenerator)<br>
- [AD FS Help](https://adfshelp.microsoft.com/)<br>
- [AD Connect Information](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-fed-management)<br>
- [Azure AD Connect Health for AD FS](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-health-adfs)
