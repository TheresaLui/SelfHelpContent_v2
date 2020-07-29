<properties
	pageTitle="Force password sync"
	description="Force password sync"
	service="microsoft.identity"
	resource=""
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="5981b983-d1be-414b-8ed3-7907a458aa82"
/>

# Force password sync

* Force a full password sync. 
* This is an invasive resort resolution step which should be tried only when absolutely necessary and all other troubleshooting attempts have failed.
* Use the steps below to force password sync

~~~powershell

$adConnector = $CASE SENSITIVE AD CONNECTOR NAME$ 
$aadConnector = $CASE SENSITIVE AAD CONNECTOR NAME$ 
Import-Module adsync 
$c = Get-ADSyncConnector -Name $adConnector 
$p = New-Object Microsoft.IdentityManagement.PowerShell.ObjectModel.ConfigurationParameter  Microsoft.Synchronize.ForceFullPasswordSync   String, ConnectorGlobal, $null, $null, $null 
$p.Value = 1 $c.GlobalParameters.Remove($p.Name) 
$c.GlobalParameters.Add($p) 
$c = Add-ADSyncConnector -Connector $c
Set-ADSyncAADPasswordSyncConfiguration -SourceConnector $adConnector TargetConnector $aadConnector -Enable $false
Set-ADSyncAADPasswordSyncConfiguration -SourceConnector $adConnector TargetConnector $aadConnector -Enable $true

~~~
