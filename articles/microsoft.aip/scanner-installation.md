<properties
	pageTitle="Azure Information Protection - Scanner Installation"
	description="Azure Information Protection - Scanner Installation"
	service="microsoft.aip"
	resource="aip"
	authors="orbarak-ms"
	ms.author="orbarak"
	articleId="Scanner_Installation"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32629559"
	resourceTags=""
	productPesIds="14997"
	cloudEnvironments="public, Fairfax"
	ownershipId="AzureIdentity_InformationProtection"
/>

# Azure Information Protection - Scanner Installation

If you are upgrading and not performing a clean installation, please make sure you have followed the guidelines for [upgrading the Azure Information Protection scanner](https://docs.microsoft.com/azure/information-protection/rms-client/client-admin-guide#upgrading-the-azure-information-protection-scanner) and for unified labeling client check [upgrading the Azure Information Protection scanner](https://docs.microsoft.com/azure/information-protection/rms-client/clientv2-admin-guide#upgrading-the-azure-information-protection-scanner).

If an alternate configuration is needed for any of the below reasons, please follow [deploy the scanner with alternative configurations](https://docs.microsoft.com/azure/information-protection/deploy-aip-scanner#deploying-the-scanner-with-alternative-configurations): 

* Servers are not allowed Internet connectivity
* You cannot be granted Sysadmin or databases must be created and configured manually
* Service accounts cannot be granted the Log on locally right
* Service accounts cannot be synchronized to Azure Active Directory but servers have Internet connectivity

Verify that you comply with all [Firewalls and network infrastructure settings requirements](https://docs.microsoft.com/azure/information-protection/requirements#firewalls-and-network-infrastructure).

If you still experience issues, please export the scanner logs and add them to your ticket. 

### How to export Azure Information Protection Scanner logs

1. Navigate to `%localappdata%\Microsoft\MSIP` under the user context running the scanner service
2. Zip all the contents under the MSIP folder
3. Save the logs to your choice of location, and attach them to your service request

## **Recommended Documents**

* [Deploying the Azure Information Protection scanner to automatically classify and protect files](https://docs.microsoft.com/azure/information-protection/deploy-aip-scanner)<br>
* [Run a discovery cycle and view reports for the scanner](https://docs.microsoft.com/azure/information-protection/deploy-aip-scanner#run-a-discovery-cycle-and-view-reports-for-the-scanner)<br>
* [Install-AIPScanner Overview](https://docs.microsoft.com/powershell/module/azureinformationprotection/install-aipscanner?view=azureipps)<br>
* [Update-AIPScanner Overview](https://docs.microsoft.com/powershell/module/azureinformationprotection/update-aipscanner?view=azureipps)<br>
* [Review Azure Information Protection documentation](https://docs.microsoft.com/azure/information-protection/what-is-information-protection)<br>
* [Requirements for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/get-started/requirements)


