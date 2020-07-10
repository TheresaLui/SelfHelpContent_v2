<properties
	pageTitle="RMS Connector - FCI"
	description="RMS Connector - FCI"
	service="microsoft.aip"
	resource="aip"
	authors="orbarak-ms"
	ms.author="orbarak,Uwe.Wizovsky"
	articleId="RMS_Connector_FCI"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32584349"
	resourceTags=""
	productPesIds="14997"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureIdentity_InformationProtection"
/>

# RMS Connector - FCI

## **Recommended Steps**

* [How File servers that run Windows Server and use File Classification Infrastructure (FCI) support Azure Rights Management](https://docs.microsoft.com/azure/information-protection/file-server-support)
* [RMS protection with Windows Server File Classification Infrastructure (FCI)](https://docs.microsoft.com/azure/information-protection/rms-client/configure-fci)

There are 2 ways of integrating FCI with AIP:

1. via the RMS Connector
2. Directly

### Via Connector

1. Make sure all the [pre-requisites are met](https://docs.microsoft.com/azure/information-protection/configure-servers-rms-connector#configuring-a-file-server-for-file-classification-infrastructure-to-use-the-connector)<br>
2. Update your [File server and File Classification Infrastructure registry settings](https://docs.microsoft.com/azure/information-protection/rms-connector-registry-settings#file-server-and-file-classification-infrastructure-registry-settings)<br>

If the above didn't help, please collect the below logs and add them to your support ticket:

1. RMS Analyzer trace run on the FCI Server when trying to pull templates or reproducing any other problem
2. The event logs of the [RMS connector servers](https://docs.microsoft.com/azure/information-protection/monitor-rms-connector)<br>
3. The [RMS connector traces](https://docs.microsoft.com/azure/information-protection/monitor-rms-connector#logging)<br>

### Directly

1. Make sure all the [pre-requisites are met](https://docs.microsoft.com/azure/information-protection/rms-client/configure-fci)<br>
2. Run the troubleshooting steps, including the commands, in PowerShell alone without the connector:

	1. [Set-RMSServerAuthentication](https://docs.microsoft.com/powershell/module/azureinformationprotection/set-rmsserverauthentication?view=azureipps)
	2. Get-RMSServer after you did step 1
	3. Get-RMSTemplate after you did step 1

If the above didn't help, please collect the below logs and add them to your support ticket:

1. Create an [RMS connector trace](https://docs.microsoft.com/azure/information-protection/monitor-rms-connector#logging)<br>
2. RMS Analyzer:<br>

	* [Download RMS Analyzer](https://www.microsoft.com/download/details.aspx?id=46437)<br>
	* Start as local admin
	* Go straight to the logging tab<br>
	* Start logging<br>
	* Reproduce the issue<br>
	* Afterwards stop logging<br>
	* Attach the create zip/cab file to the support call and explain what you are trying to do<br>

## **Recommended Documents**

* [What’s the difference between Windows Server FCI and the Azure Information Protection scanner?](https://docs.microsoft.com/azure/information-protection/faqs#whats-the-difference-between-windows-server-fci-and-the-azure-information-protection-scanner)<br>
* [Deploying the Azure Rights Management connector](https://docs.microsoft.com/azure/information-protection/deploy-rms-connector )<br>
* [Installing and configuring the Azure Rights Management connector](https://docs.microsoft.com/azure/information-protection/install-configure-rms-connector)<br>
* [Monitor the Azure Rights Management connector](https://docs.microsoft.com/azure/information-protection/monitor-rms-connector)<br>
* [Configuring servers for the Azure Rights Management connector](https://docs.microsoft.com/azure/information-protection/configure-servers-rms-connector)<br>
* [Registry setting for the Rights Management connector](https://docs.microsoft.com/azure/information-protection/rms-connector-registry-settings)
