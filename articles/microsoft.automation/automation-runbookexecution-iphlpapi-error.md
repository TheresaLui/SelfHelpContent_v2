<properties
	pageTitle="Runbook Execution/Runbook fails with iphlpapi error"
	description="Runbook Execution/Runbook fails with iphlpapi error"
	infoBubbleText="This runbook was seen to fail with iphlpapi error"
	service="microsoft.automation"
	resource="runbook"
	ms.author="bmcder"
	displayOrder=""
	articleId="aea2c39f-c93f-4e78-bc45-d9b3e7b29034"
	diagnosticScenario=""
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15607"
	cloudEnvironments="public,blackForest,fairfax,mooncake,ussec,usnat"
	ownershipId="Compute_Automation"
/>

# We ran diagnostics and found that this runbook failed with the following error "Unable to find an entry point named 'GetPerAdapterInfo' in DLL 'iphlpapi.dll'"

## Runbook failed with the following error "Unable to find an entry point named 'GetPerAdapterInfo' in DLL 'iphlpapi.dll'"
<!--issueDescription-->
This runbook <!--$tokenname-->[AutomationRunbookName]<!--/$tokenname--> failed with the following error "Unable to find an entry point named 'GetPerAdapterInfo' in DLL 'iphlpapi.dll'"

This error is reported when the runbook tries to make a call into that dll on an Azure Runbook Worker, but as that dll doesn't exist in a sandbox environment it fails. This is typically seen following a remote authentication failure and it is typically the authentication issue that you need to troubleshoot.
<!--/issueDescription-->

## **Recommended Steps**

### Failure to authenticate with credential + password

If this error is seen following a call to a cmdlet that is authenticating using credentials (i.e. not using a service principal with a certificate), e.g: 

- Add-AzAccount
- Connect-AzureRmAccount
- Add-AzureAnalysisServicesAccount 
- Connect-PnPOnline

1. Confirm that the password/username in the credential are correct and that the password hasn't expired
2. Check if someone has [enabled Conditional Access to Azure AD](https://docs.microsoft.com/azure/active-directory/conditional-access/overview) as this too can break authentication and result in this error
3. If the username/password is confirmed as being good but this has never worked then have change the code to use a service principal with a certificate for authentication instead of a credential with a password, for example: 

```
$Conn = Get-AutomationConnection -Name AzureRunAsConnection
Connect-AzAccount `
-ServicePrincipal `
-Tenant $Conn.TenantID `
-ApplicationID $Conn.ApplicationID `
-CertificateThumbprint $Conn.CertificateThumbprint
```

or

```
$connectionName = "AzureRunAsConnection"
$servicePrincipalConnection = Get-AutomationConnection -Name $connectionName
Add-AzureAnalysisServicesAccount -RolloutEnvironment 'westus2.asazure.windows.net' -ServicePrincipal -CertificateThumbprint $servicePrincipalConnection.CertificateThumbprint -TenantId $servicePrincipalConnection.TenantId -ApplicationId $servicePrincipalConnection.ApplicationId 
Write-Output "Added account"
Sync-AzureAnalysisServicesInstance -Instance 'asazure://westus2.asazure.windows.net/analysis:rw' -Database adventureworks
ZA
```

### The account requires Multi Factor Authentication (MFA)

If the account is using MFA then this will **never** **work** in an Automation scenario as a background job has no way to provide a new form of authentication when prompted.

### This error is seen and it doesn't occur following an authentication failure

Test out the code on a Hybrid Runbook Worker as the iphlpapi dll is available in that environment.

## **Recommended Documents**

* [Manage credentials in Azure Automation](https://docs.microsoft.com/azure/automation/shared-resources/credentials)
* [Configure authentication with Azure AD](https://docs.microsoft.com/azure/automation/automation-use-azure-ad)
* [Conditional Access to Azure AD](https://docs.microsoft.com/azure/active-directory/conditional-access/overview)
* [Azure Multi-Factor Authentication](https://docs.microsoft.com/azure/active-directory/authentication/concept-mfa-howitworks)
