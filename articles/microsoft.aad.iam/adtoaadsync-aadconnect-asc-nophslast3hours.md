<properties
	pageTitle="AAD Connect server(s) did not sync passwords in the last 3 hours"
	description="No password sync in last 3 hours"
	infoBubbleText="No password sync in last 3 hours. See details on the right"
	service="microsoft.aad.iam"
	resource="aadconnect"
	authors="jecheria"
	displayOrder="1"
	articleId="ADtoAADSync_AADConnect_ASC_No_PasswordHashSynchronization_3Hours"
	diagnosticScenario=""
	selfHelpType="Diagnostics"
	resourceTags=""
	productPesIds="14785"
	cloudEnvironments="public"
/>
# AAD Connect server(s) did not sync passwords in the last 3 hours
<!--issueDescription-->
## AAD Connect server(s) did not sync passwords in the last 3 hours

We detected that there has not been any password hash sync activity received for your tenant in the past 3 hours. This indicates that there is an issue with your on premises password synchronization feature.

## **Recommended steps**
To investigate the root cause of the issue and find how you can resolve this, you can use the Azure AD Connect password hash synchronization troubleshooter. In the following article we explain how to run the troubleshooter and how to interpret the results and resolve the issue:
[Troubleshoot password hash synchronization with Azure AD Connect sync](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-troubleshoot-password-hash-synchronization)
