<properties
	pageTitle="Azure Information Protection - Discovery Reporting Issues"
	description="Azure Information Protection - Discovery Reporting Issues"
	service="microsoft.aip"
	resource="aip"
	authors="orbarak-ms"
	ms.author="orbarak"
	articleId="Scanner_Discovery_Reporting_Issues"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32629556"
	resourceTags=""
	productPesIds="14997"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureIdentity_InformationProtection"
/>

# Azure Information Protection - Discovery Reporting Issues

## **Recommended Steps**

1. If you used the [built-in information types](https://support.office.com/article/What-the-sensitive-information-types-look-for-fd505979-76be-4d9f-b459-abef3fc9e86b) for your Azure Information Protection policy, verify that your content matches the expected format
2. Verify that the label is appropriately configured for **Automatic** or **Recommended**
3. Note that **Automatic** labeling is available for all Office apps, whereas **Recommended** is available for all Office apps except for Outlook
4. Verify that the user account configured to run the scanner service has permissions to access all the configured repositories

If you are still experiencing the issue, collect Azure Information Protection scanner logs and attach the logs to this ticket.

### How to export Azure Information Protection Scanner logs

1. Navigate to `%localappdata%\Microsoft\MSIP` under the user context running the scanner service
2. Zip all the contents under the MSIP folder
3. Save the logs to your choice of location, and attach them to your service request


## **Recommended Documents**

* [Deploying the Azure Information Protection scanner to automatically classify and protect files](https://docs.microsoft.com/azure/information-protection/deploy-aip-scanner)<br>
* [Run a discovery cycle and view reports for the scanner](https://docs.microsoft.com/azure/information-protection/deploy-aip-scanner#run-a-discovery-cycle-and-view-reports-for-the-scanner)<br>
* [Install-AIPScanner Overview](https://docs.microsoft.com/powershell/module/azureinformationprotection/install-aipscanner?view=azureipps)<br>
* [Review Azure Information Protection documentation](https://docs.microsoft.com/azure/information-protection/what-is-information-protection)<br>
* [Requirements for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/get-started/requirements)
