<properties
	pageTitle="Connect to vCenter errors"
	description="Errors when connecting to vCenter server from the collector"
	service="microsoft.migrate"
	resource="projects"
	authors="shijojoy"
	ms.author="shijoy"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32631904"
	resourceTags=""
	productPesIds="16348"
	cloudEnvironments="public"
	articleId="808d9835-421f-4aba-9a6a-b11625796206"
/>

# I cannot connect to vCenter server

## **Recommended Steps**

* **Error: UnhandledException. Description: Internal error occured: System.IO.FileNotFoundException Message**

	When you get this error follow below steps to resolve:

	1. If you are not on the latest Collector version, upgrade the Collector to the [latest version](https://docs.microsoft.com/azure/migrate/concepts-collector#how-to-upgrade-collector) and check if the issue is resolved
	2. If you already have the latest Collector version, then manually install [VMware PowerCLI 6.5.2](https://www.powershellgallery.com/packages/VMware.PowerCLI/6.5.2.6268016) and check if the issue is resolved
	3. If that does not work, remove `VMware.Vim.dll` and `VimService65.dll` dlls present in the `C:\Program Files\ProfilerService` folder and restart the Azure Migrate Collector service

* Unable to connect to vCenter Server "Servername.com:9443**

	Unable to connect to vCenter Server "Servername.com:9443" due to error: There was no endpoint listening at https://Servername.com:9443/sdk that could accept the message.

	This happens when the Collector machine is unable to resolve the vCenter server name specified or the port specified is wrong. By default, if the port is not specified, the Collector will try to connect to the port number 443.

	Please follow below steps to check connection:

	1. Try to ping the Servername.com from the Collector machine
	2. If step 1 fails, try to connect to the vCenter server over IP address
	3. If vCenter server is configured with non-default port, identify the correct port number to connect to the vCenter
	4. Finally check if the vCenter server is up and running
