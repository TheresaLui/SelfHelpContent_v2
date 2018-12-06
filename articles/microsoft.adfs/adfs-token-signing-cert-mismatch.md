<properties
	pageTitle="AD FS Sign-In Error - Token Signing Certificate Mismatch"
	description="This page describes the CRC for sign in errors due to a mismatch in the token signing certificate between AD FS and Azure AD"
	infoBubbleText="Found recent login failures. See details on the right."
	service="Microsoft.Adfs"
	resource="Tenant"
	authors="madhavpatel6"
	displayOrder="1"
	articleId="adfs_token_signing_cert_mismatch"
	diagnosticScenario="ADFS - Token Signing Cert Mismatch"
	selfHelpType="diagnostics"
	supportTopicIds="32045775"
	resourceTags=""
	productPesIds="14785"
	cloudEnvironments="public, BlackForest, Fairfax, MoonCake"
/>

# Sign-In issues into Azure AD with AD FS due a mismatch of the token signing certificate

We have detected sign-in issues for one or more of your federated domains. This is occurring due to a mismatch between the token signing certificate that AD FS is using to issue authentication tokens and the public key that Azure AD is using to validate the tokens. This error could happen due to your federation metadata not being available externally. In addition to the steps below, verify that the metadata is available by using the [Federation Metadata Explorer](https://adfshelp.microsoft.com/MetadataExplorer/GetFederationMetadata) tool. We detected the following domains that are experiencing these failures: <!--$Domains-->

### Recommended solution
We recommend using PowerShell to easily resolve this issue. Follow the steps below to resolve your issue:

1. On your AD FS server, launch a PowerShell window.

2. If you haven't installed the `MSOnline` module, run the following to install it.

```
Install-Module MSOnline
```

3. Run the following to import the module.

```
Import-Module MSOnline
```

4. We will be making changes to the configuration in Azure AD, so we will need to connect to Azure AD. Run the following cmdlet and login with a global administrator account.

```
Connect-MsolService
```

5. Run the following snippet to manually check the token signing certificates configured on AD FS and the Azure AD trust properties for all of your federated domains. In the output each domain should have the same token signing certificate for both sources ("ADFS Server" and "Microsoft Office 365")

```
Get-MsolDomain -Authentication Federated | Foreach {
    Write-Host "Checking domain" $_.Name
    Get-MsolFederationProperty -DomainName $_.Name | Format-List Source, TokenSigningCertificate
}
```

7. For each domain run the following cmdlet. This cmdlet updates the settings from AD FS into the cloud service and configures the trust relationship between the two.

```
Update-MSOLFederatedDomain –DomainName <domain>
```