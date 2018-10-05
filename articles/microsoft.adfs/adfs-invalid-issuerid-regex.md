<properties
	pageTitle="AD FS Sign-In Error - Issuer Id Claim Rule"
	description="This page describes the CRC for sign in errors due to improper AD FS IssuerID claim rule"
	infoBubbleText="Found recent login failures. See details on the right."
	service="microsoft.adfs"
	resource="Tenant"
	authors="madhavpatel6"
	displayOrder="1"
	articleId="adfs_invalid_issuerid_regex"
	selfHelpType="diagnostics"
	supportTopicIds="32045775"
	resourceTags=""
	productPesIds="14785"
	cloudEnvironments="public, BlackForest, Fairfax, MoonCake"
/>

# Sign-In issues into Azure AD with AD FS due to improper IssuerID claim rule

## What is the issue?
We have detected sign-in issues for one or more of your federated domains. This is occurring due to a misconfiguration on your federation trust with Azure AD. <!-- Should we add more information about IssuerID? -->

## How do I fix the issue?

### Recommended solution
We recommend using [Azure AD Connect](https://docs.microsoft.com/en-us/azure/active-directory/connect/active-directory-aadconnect) to easily resolve this issue. Azure AD Connect provides a way that you can reset the federation trust between Azure AD and AD FS. The following article will guide you through resetting your federation trust: [Repair the federation trust between Azure AD and AD FS](https://docs.microsoft.com/en-us/azure/active-directory/connect/active-directory-aadconnect-federation-management)

`If you have custom claim rules in your federation trust with Azure AD, they will get overwritten by Azure AD Connect. If custom claims rules are present, before repairing the federation trust using Azure AD Connect you can export the claims rules and then import them anew after the repair.`

### Alternative solution
If you are not managing AD FS with Azure AD Connect, we recommend that you use [Azure AD RPT Claim Rules](https://adfshelp.microsoft.com/AadTrustClaims/ClaimsGenerator).

1. To generate the right set of claims for your organization, it will ask you a few questions about your AAD Connect configuration.

2. At the end, you will be provided with the correct set of claim rules for your federation trust. A PowerShell script will help you easily set the claim rules.