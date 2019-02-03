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
	cloudEnvironments="public"
/>

# RMS Connector - FCI

## Recommended troubleshooting steps

Please read the following 2 links:
[How File servers that run Windows Server and use File Classification Infrastructure (FCI) support Azure Rights Management](https://docs.microsoft.com/azure/information-protection/file-server-support)<br>
[RMS protection with Windows Server File Classification Infrastructure (FCI)](https://docs.microsoft.com/azure/information-protection/rms-client/configure-fci)


There are 2 ways of integrating FCI with AIP

1. via the RMS Connector.
1. via the RMS Connector.
2. Directly

Via Connector

Make sure all the pre-requisites are met on this link [Configuring a file server for File Classification Infrastructure to use the connector](https://docs.microsoft.com/azure/information-protection/configure-servers-rms-connector#configuring-a-file-server-for-file-classification-infrastructure-to-use-the-connector)<br>
Make sure you have the settings in registry correctly: [File server and File Classification Infrastructure registry settings](https://docs.microsoft.com/azure/information-protection/rms-connector-registry-settings#file-server-and-file-classification-infrastructure-registry-settings)<br>

In a worst case scenario, we need the following information:

1. RMS Analyzer trace run on the FCI Server when trying to pull templates or reproducing any other problem
2. The event logs of the RMS connector servers as outlined here: [Monitor the Azure Rights Management connector](https://docs.microsoft.com/azure/information-protection/monitor-rms-connector)<br>
3. The RMS connector traces as described here: [Logging](https://docs.microsoft.com/azure/information-protection/monitor-rms-connector#logging)<br>

all 3 need to be from the same time.

Directly
please meet all the pre-reqs here: [RMS protection with Windows Server File Classification Infrastructure (FCI)](https://docs.microsoft.com/azure/information-protection/rms-client/configure-fci)<br>

Troubleshooting steps including running the commands in PS alone, without the connector.

1. set-rmsserverauthentication  as described here: [Set-RMSServerAuthentication](https://docs.microsoft.com/powershell/module/azureinformationprotection/set-rmsserverauthentication?view=azureipps)
2. get-rmsserver after you did step 1
3. get-rmstemplate after you did step 1


If all of the above didn't help, please collect the below logs and add them to your suppot ticket

Create an RMS connector Trace 
RMS connector as described here:
[Logging](https://docs.microsoft.com/azure/information-protection/monitor-rms-connector#logging)<br>

RMS Analyzer:
Download from here: [Download RMS Analyzer](https://www.microsoft.com/download/details.aspx?id=46437)
Start as local admin.
Go straight to the logging tab
Start logging
Reproduce the issue
Afterwards stop logging
Attach the create zip/cab file to the support call and explain what you are trying to do



## **Recommended Documents**

[What’s the difference between Windows Server FCI and the Azure Information Protection scanner?](https://docs.microsoft.com/azure/information-protection/faqs#whats-the-difference-between-windows-server-fci-and-the-azure-information-protection-scanner)<br>
[Deploying the Azure Rights Management connector](https://docs.microsoft.com/azure/information-protection/deploy-rms-connector )<br>
[Installing and configuring the Azure Rights Management connector](https://docs.microsoft.com/azure/information-protection/install-configure-rms-connector)<br>
[Monitor the Azure Rights Management connector](https://docs.microsoft.com/azure/information-protection/monitor-rms-connector)<br>
[Configuring servers for the Azure Rights Management connector](https://docs.microsoft.com/azure/information-protection/configure-servers-rms-connector)<br>
[Registry setting for the Rights Management connector](https://docs.microsoft.com/azure/information-protection/rms-connector-registry-settings)