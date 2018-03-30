<properties
	pageTitle="The account I used for the Intune Exchange Connector cannot communicate with our exchange server"
	description="The account I used for the Intune Exchange Connector cannot communicate with our exchange server"
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

# The account I used for the Intune Exchange Connector cannot communicate with our exchange server

## **Recommended steps**

You must create an Active Directory user account that is used by the Intune Exchange Connector. The account must have permission to run the following required Windows PowerShell Exchange cmdlets:

* Get-ActiveSyncOrganizationSettings, Set-ActiveSyncOrganizationSettings
* Get-CasMailbox, Set-CasMailbox
* Get-ActiveSyncMailboxPolicy, Set-ActiveSyncMailboxPolicy, New-ActiveSyncMailboxPolicy, Remove-ActiveSyncMailboxPolicy
* Get-ActiveSyncDeviceAccessRule, Set-ActiveSyncDeviceAccessRule, New-ActiveSyncDeviceAccessRule, Remove-*ActiveSyncDeviceAccessRule
* Get-ActiveSyncDeviceStatistics
* Get-ActiveSyncDevice
* Get-ExchangeServer
* Get-ActiveSyncDeviceClass
* Get-Recipient
* Clear-ActiveSyncDevice, Remove-ActiveSyncDevice
* Set-ADServerSettings
* Get-Command

For more infomration please review [this document](https://docs.microsoft.com/intune/exchange-connector-install#exchange-cmdlet-requirements).


