<properties
	pageTitle="Azure Information Protection - Installing, Onboarding, or Decommissioning - AIP Scanner Installation and Configuration"
	description="Azure Information Protection - Installing, Onboarding, or Decommissioning - AIP Scanner Installation and Configuration"
	service="microsoft.aip"
	resource="aip"
	authors="orbarak-ms"
	ms.author="orbarak"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32727933"
	resourceTags=""
	productPesIds="14997"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
	articleId="MIP_Onboard_Scanner_Install_config"
	ownershipId="AzureIdentity_InformationProtection"
/>

# Azure Information Protection  - Installing, Onboarding, or Decommissioning - AIP Scanner Installation and Configuration

## **Recommended Steps**

1. If you are upgrading and not performing a clean installation, please make sure you have followed the guidelines for [upgrading the Azure Information Protection scanner](https://docs.microsoft.com/azure/information-protection/rms-client/client-admin-guide#upgrading-the-azure-information-protection-scanner) and for unified labeling client check [upgrading the Azure Information Protection scanner](https://docs.microsoft.com/azure/information-protection/rms-client/clientv2-admin-guide#upgrading-the-azure-information-protection-scanner)
2. Verify that you comply with all [Firewalls and network infrastructure settings requirements](https://docs.microsoft.com/azure/information-protection/requirements#firewalls-and-network-infrastructure)
3. Make sure your [policies are set](https://docs.microsoft.com/azure/information-protection/configure-policy) to automatic labeling or have a default label in the policy
4. Make sure that the relevant file type is configured for label/protection as described here: [File types supported by the Azure Information Protection client](https://docs.microsoft.com/azure/information-protection/rms-client/client-admin-guide-file-types#supported-file-types-for-classification-and-protection). In addition, if you want to change the default behavior, follow this guidelines: [Changing the default protection level of files](https://docs.microsoft.com/azure/information-protection/rms-client/client-admin-guide-file-types#changing-the-default-protection-level-of-files)
5. Verify that the user account configured to run the scanner service has permissions to access all the configured repositories
6. Run [Start-AIPScannerDiagnostics](https://docs.microsoft.com/powershell/module/azureinformationprotection/start-aipscannerdiagnostics?view=azureipps) in order to troubleshoot common issues when deploying scanner
7. If you still experience issues, please export the scanner logs and add them to your ticket

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

