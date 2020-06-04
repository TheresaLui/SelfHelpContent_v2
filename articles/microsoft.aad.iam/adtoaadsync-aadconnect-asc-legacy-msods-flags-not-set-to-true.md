<properties
pageTitle="Legacy MSODS flag(s) have their value not set to 'true'"
	description="Legacy MSODS flag(s) have their value not set to 'true'"
	infoBubbleText="Legacy MSODS flag(s) have their value not set to 'true'"
	service="microsoft.aad.iam"
	resource="aadconnect"
	authors="rodejo"
	ms.author="rodejo"
	displayOrder="1"
	articleId="ADtoAADSync_AADConnect_ASC_LegacyMSODSFlagsNotSetToTrue"
	diagnosticScenario=""
	selfHelpType="Diagnostics"
	resourceTags=""
	productPesIds="16666"
  cloudEnvironments="public, Fairfax, Mooncake, ussec, usnat"
  ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# Legacy MSODS flag(s) have their value not set to "true"
<!--issueDescription-->
The following legacy MSODS flag(s) on this tenant have their value not set to "true": <!--$IssueDetails-->[IssueDetails]<!--/$IssueDetails-->
<!--/issueDescription-->

## **Recommended Steps**
Please set the flags to "true". A further explanation about the importance of these flags and how to set them can be found here
- [Azure AD Connect sync service features](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-syncservice-features)
- [EnableSoftMatchOnUpn](https://support.microsoft.com/help/3164442/how-to-use-upn-matching-for-identity-synchronization-in-office-365-azu)
- [SynchronizeUpnForManagedUsers](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-syncservice-features#synchronize-userprincipalname-updates)
- [DuplicateProxyAddressResiliency](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-syncservice-duplicate-attribute-resiliency#enabling-duplicate-attribute-resiliency)
- [DuplicateUPNResiliency](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-syncservice-features#duplicate-attribute-resiliency)
