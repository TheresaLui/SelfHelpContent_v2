<properties
	pageTitle="The account used for the Exchange Connector cannot communicate with our Microsoft Exchange Server"
	description="The account used for the Exchange Connector cannot communicate with our Microsoft Exchange Server"
	service="microsoft.intune"
	resource="intune"
	authors="mackie1604"
	displayOrder="2"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="onpremise_selfhelp"
	productPesIds=""
	cloudEnvironments="public"
/>

# The account used for the Exchange Connector cannot communicate with our Microsoft Exchange Server.

## **Recommended steps**

Create an Active Directory user account for the Intune on-premises Exchange Connector.  The account must have permission to run the following required Windows PowerShell Exchange cmdlets:

* Get-ActiveSyncOrganizationSettings, Set-ActiveSyncOrganizationSettings
* Get-CasMailbox, Set-CasMailbox
* Get-ActiveSyncMailboxPolicy, Set-ActiveSyncMailboxPolicy, New-ActiveSyncMailboxPolicy, Remove-ActiveSyncMailboxPolicy
* Get-ActiveSyncDeviceAccessRule, Set-ActiveSyncDeviceAccessRule, New-ActiveSyncDeviceAccessRule, Remove-ActiveSyncDeviceAccessRule
* Get-ActiveSyncDeviceStatistics
* Get-ActiveSyncDevice
* Get-ExchangeServer
* Get-ActiveSyncDeviceClass
* Get-Recipient
* Clear-ActiveSyncDevice, Remove-ActiveSyncDevice
* Set-ADServerSettings
* Get-Command


