<properties
	pageTitle="Azure Information Protection - Protecting and Opening Content - Questions about applying protection with AIP Scanner"
	description="Azure Information Protection - Protecting and Opening Content - Questions about applying protection with AIP Scanner"
	service="microsoft.aip"
	resource="aip"
	authors="orbarak-ms"
	ms.author="orbarak"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32727962"
	resourceTags=""
	productPesIds="14997"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
	articleId="protectopencontent_scannerprotect"
	ownershipId="AzureIdentity_InformationProtection"
/>

# Azure Information Protection Protection - Protecting and Opening Content - Questions about applying protection with AIP Scanner

## **Recommended Steps**

Run [Start-AIPScannerDiagnostics](https://docs.microsoft.com/powershell/module/azureinformationprotection/start-aipscannerdiagnostics?view=azureipps) in order to troubleshoot common issues when deploying scanner.

### Export Azure Information Protection Scanner logs

1. Navigate to `%localappdata%\Microsoft\MSIP` under the user context running the scanner service 
2. Zip all the contents under the MSIP folder
3. Save the logs to your choice of location, and attach them to your service request
4. You can also use [Export-AIPLogs -OnBehalfOf](https://docs.microsoft.com/powershell/module/azureinformationprotection/export-aiplogs?view=azureipps)

## **Recommended Documents**

* [Configure the scanner to apply classification and protection](https://docs.microsoft.com/azure/information-protection/deploy-aip-scanner#configure-the-scanner-to-apply-classification-and-protection)<br>
* [Review Azure Information Protection documentation](https://docs.microsoft.com/azure/information-protection/what-is-information-protection)<br>
* [Review Azure Information Protection subscriptions and features](https://azure.microsoft.com/pricing/details/information-protection)<br>
* [How Office applications and services support Azure Rights Management](https://docs.microsoft.com/azure/information-protection/office-apps-services-support)<br>
* [Applications that support Azure Rights Management data protection](https://docs.microsoft.com/azure/information-protection/requirements-applications)<br>
* [Requirements for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/get-started/requirements)<br>
* [Quick start tutorial for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/get-started/infoprotect-quick-start-tutorial)<br>
* [Download Azure Information Protection client](https://www.microsoft.com/download/details.aspx?id=53018)<br>

