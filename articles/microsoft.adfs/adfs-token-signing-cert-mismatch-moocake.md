<properties
	pageTitle="AD FS Sign-In Error - Token Signing Certificate Mismatch"
	description="This page describes the CRC for sign in errors due to a mismatch in the token signing certificate between AD FS and Azure AD"
	infoBubbleText="Found recent login failures. See details on the right."
	service="Microsoft.Adfs"
	resource="Tenant"
	authors="madhavpatel6"
    ms.author="madpatel"
	displayOrder="2"
	articleId="adfs-token-signing-cert-mismatch-moocake"
	diagnosticScenario="ADFS - Token Signing Cert Mismatch"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="MoonCake"
	ownershipId="AzureIdentity_SignIn"
/>

# Sign-In issues into Azure AD with AD FS due a mismatch of the token signing certificate
<!--/issueDescription-->
We have detected sign-in issues for one or more of your federated domains. This is caused by a mismatch between the token signing certificate that AD FS is using to issue authentication tokens and the public key that Azure AD is using to validate the tokens. This error could occur due to your federation metadata not being available externally.
<!--/issueDescription-->

We detected the following domains are experiencing failures:

**<!--$Domains-->Domains<!--/$Domains-->**

## **Recommended Steps**

In PowerShell:

1. On your AD FS server, launch a PowerShell window
2. If you haven't installed the **MSOnline** module, run the following cmdlet to install it: `Install-Module MSOnline`
3. Run the following cmdlet to import the module: `Import-Module MSOnline`
4. We will be making changes to the configuration in Azure AD, so we will need to connect to Azure AD. Run the following cmdlet and login with a global administrator account: `Connect-MsolService`
5. We will need to make sure we update all your federated domains that are having this issue. There are two options on how to get the misconfigured domains:

    * Run **Snippet 1** to automatically check that the token signing certificate matches for all of your federated domains. Upon completion, you will have a list of all the domains that have a mismatch.
    * Run **Snippet 2** to manually check the token signing certificates configured on AD FS and the Azure AD trust properties for all your federated domains. In the output, each domain should have the same token signing certificate for both sources ("ADFS Server" and "Microsoft Office 365").

6. For each misconfigured domain, run the following cmdlet. This cmdlet updates the settings from AD FS into the cloud service and configures the trust relationship between the two: `Update-MSOLFederatedDomain –DomainName <domain>`
7. Verify that the metadata is available by using the [Federation Metadata Explorer](https://adfshelp.microsoft.com/MetadataExplorer/GetFederationMetadata) tool

### Snippet 1

```
$mismatchedDomains = @()
Get-MsolDomain -Authentication Federated | Foreach {
		$setting = Get-MsolFederationProperty -DomainName $_.Name
		if ($setting[0].TokenSigningCertificate -ne $setting[1].TokenSigningCertificate) {
				$mismatchedDomains += $_.Name
		}
}
if ($mismatchedDomains.Length -eq 0) {
		"All of your domains are properly configured" | Out-String
} else {
		$domainString = $mismatchedDomains -join ", "
		"Detected the following domains had a mismatch: $domainString" | Out-String
}
```

### Snippet 2

```
Get-MsolDomain -Authentication Federated | Foreach {
		Write-Host "Checking domain" $_.Name
		Get-MsolFederationProperty -DomainName $_.Name | Format-List Source, FederationServiceDisplayName, TokenSigningCertificate
}
```
