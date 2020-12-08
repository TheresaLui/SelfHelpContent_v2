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

# Azure Information Protection Protection - Protecting and Opening Content - Questions about applying protection with the AIP Scanner

To provide a unified and streamlined customer experience, the classic client and label management in the Azure Portal are being deprecated as of March 31, 2021. Learn more in the [official deprecation notice](https://techcommunity.microsoft.com/t5/microsoft-security-and/announcing-timelines-for-sunsetting-label-management-in-the/ba-p/1226179).

## **Recommended Steps**

If you are running the scanner installed with the unified labeling client, run [Start-AIPScannerDiagnostics](https://docs.microsoft.com/powershell/module/azureinformationprotection/start-aipscannerdiagnostics?view=azureipps) to troubleshoot common deployment issues.

### Export Azure Information Protection Scanner logs

Regardless of whether you're using the unified labeling or classic client, export scanner logs as follows:

1. Navigate to `%localappdata%\Microsoft\MSIP`, for the user that's running the scanner service.
1. Zip all the contents in the **MSIP** folder.
1. Save the logs to a location of your choice, and then attach them to your service request.

**Tip**: If you are not currently logged in as the user running the scanner service, use the [Export-AIPLogs -OnBehalfOf](https://docs.microsoft.com/powershell/module/azureinformationprotection/export-aiplogs?view=azureipps) cmdlet to export logs.

## **Recommended Documents**

* [Configure the scanner to apply classification and protection](https://docs.microsoft.com/azure/information-protection/deploy-aip-scanner-configure-install#configure-the-scanner-to-apply-classification-and-protection)<br>
* [Azure Information Protection documentation](https://docs.microsoft.com/azure/information-protection/what-is-information-protection)<br>
* [Azure Information Protection subscriptions and features](https://azure.microsoft.com/pricing/details/information-protection)<br>
* [How Office applications and services support Azure Rights Management](https://docs.microsoft.com/azure/information-protection/office-apps-services-support)<br>
* [Applications that support Azure Rights Management data protection](https://docs.microsoft.com/azure/information-protection/requirements-applications)<br>
* [Requirements for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/get-started/requirements)<br>
* [Download the Azure Information Protection client](https://www.microsoft.com/download/details.aspx?id=53018)<br>

