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

## **Recommended Steps**

Follow [Upgrading the Azure Information Protection scanner](https://docs.microsoft.com/azure/information-protection/rms-client/client-admin-guide#upgrading-the-azure-information-protection-scanner)

### Export Azure Information Protection Scanner logs

1. Navigate to `%localappdata%\Microsoft\MSIP` under the user context running the scanner service 
2. Zip all the contents under the MSIP folder
3. Save the logs to your choice of location, and attach them to your service request
4. You can also use [Export-AIPLogs -OnBehalfOf](https://docs.microsoft.com/powershell/module/azureinformationprotection/export-aiplogs?view=azureipps)

## **Recommended Documents**

* [Deploying the Azure Information Protection scanner to automatically classify and protect files](https://docs.microsoft.com/azure/information-protection/deploy-aip-scanner)<br>
* [Specify and use the Token parameter for Set-AIPAuthentication](https://docs.microsoft.com/azure/information-protection/rms-client/client-admin-guide-powershell#specify-and-use-the-token-parameter-for-set-aipauthentication)<br>
* [Run a discovery cycle and view reports for the scanner](https://docs.microsoft.com/azure/information-protection/deploy-aip-scanner#run-a-discovery-cycle-and-view-reports-for-the-scanner)<br>
* [Review Azure Information Protection documentation](https://docs.microsoft.com/azure/information-protection/what-is-information-protection)<br>
* [Requirements for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/get-started/requirements)<br>
* [Download Azure Information Protection client](https://www.microsoft.com/download/details.aspx?id=53018)

