<properties
	pageTitle="Azure Information Protection - Upgrading and Migration - Upgrade AIP Scanner Classic"
	description="Azure Information Protection - Upgrading and Migration - Upgrade AIP Scanner Classic"
	service="microsoft.aip"
	resource="aip"
	authors="orbarak-ms"
	ms.author="orbarak"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32727976"
	resourceTags=""
	productPesIds="14997"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
	articleId="MIP_Upgrading_Scanner_Classic"
	ownershipId="AzureIdentity_InformationProtection"
/>

# Azure Information Protection  - Upgrading and Migration - Upgrade AIP Scanner Classic

This article is relevant for the Azure Information Protection classic client only. 

To provide a unified and streamlined customer experience, the classic client and label management in the Azure Portal are being deprecated as of March 31, 2021. Learn more in the [official deprecation notice](https://techcommunity.microsoft.com/t5/microsoft-security-and/announcing-timelines-for-sunsetting-label-management-in-the/ba-p/1226179).

## **Recommended Steps**

Follow the steps at [Upgrading the Azure Information Protection scanner](https://docs.microsoft.com/azure/information-protection/rms-client/client-admin-guide#upgrading-the-azure-information-protection-scanner).

### Export Azure Information Protection Scanner logs

1. In the user directory for the user that is running the scanner service, navigate to `%localappdata%\Microsoft\MSIP`.
2. Zip all the contents under the **MSIP** folder.
3. Save the logs to your choice of location, and attach them to your service request.

**Tip**: You can also use [Export-AIPLogs -OnBehalfOf](https://docs.microsoft.com/powershell/module/azureinformationprotection/export-aiplogs) to export your logs via PowerShell.

## **Recommended Documents**

* [Deploying the Azure Information Protection scanner to automatically classify and protect files](https://docs.microsoft.com/azure/information-protection/deploy-aip-scanner-classic)<br>
* [Specify and use the Token parameter for Set-AIPAuthentication](https://docs.microsoft.com/azure/information-protection/rms-client/client-admin-guide-powershell#specify-and-use-the-token-parameter-for-set-aipauthentication)<br>
* [Run a discovery cycle and view reports for the scanner](https://docs.microsoft.com/azure/information-protection/deploy-aip-scanner-manage-classic)<br>
* [Azure Information Protection documentation](https://docs.microsoft.com/azure/information-protection/what-is-information-protection)<br>
* [Requirements for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/get-started/requirements)<br>
* [Download the Azure Information Protection client](https://www.microsoft.com/download/details.aspx?id=53018)

