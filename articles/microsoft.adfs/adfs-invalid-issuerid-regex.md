<properties
	pageTitle="AD FS Sign-In Error - Issuer ID Claim Rule"
	description="This page describes the CRC for sign in errors due to improper AD FS IssuerID claim rule"
	infoBubbleText="Found recent login failures. See details on the right."
	service="Microsoft.Adfs"
	resource="Tenant"
	authors="madhavpatel6"
	ms.author="madpatel"
	displayOrder="1"
	articleId="adfs_invalid_issuerid_regex"
	diagnosticScenario="ADFS - Invalid IssuerID Regex"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, BlackForest, Fairfax, MoonCake, usnat, ussec"
	ownershipId="AzureIdentity_AuthReach_HybridAuthentication"
/>

# Sign-In issues into Azure AD with AD FS due to improper IssuerID claim rule
<!--issueDescription-->
We have detected sign-in issues for one or more of your federated domains. This is occurring due to a misconfiguration on your federation trust with Azure AD. Please take a look at the following recommendations on resolving this issue.
<!--/issueDescription-->

## **Recommended Steps**

Use [Azure AD Connect](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect) to easily resolve this issue. Azure AD Connect provides a way that you can reset the federation trust between Azure AD and AD FS. If you have custom claim rules in your federation trust with Azure AD, they will get overwritten by Azure AD Connect. If custom claims rules are present, before repairing the federation trust using Azure AD Connect you can export the claims rules and then import them anew after the repair.

If you are not managing AD FS with Azure AD Connect, we recommend that you use [Azure AD RPT Claim Rules](https://adfshelp.microsoft.com/AadTrustClaims/ClaimsGenerator):

1. To generate the right set of claims for your organization, it will ask you a few questions about your AAD Connect configuration
2. At the end, you will be provided with the correct set of claim rules for your federation trust. A PowerShell script will help you easily set the claim rules.

## **Recommended Documents**

* [Repair the federation trust between Azure AD and AD FS](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-federation-management)