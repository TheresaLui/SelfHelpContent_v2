<properties
	pageTitle="Connect to vCenter errors"
	description="Errors when connecting to vCenter server from the collector"
	service="microsoft.migrate"
	resource="projects"
	authors="ruturaj"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32593686, 32593696"
	resourceTags=""
	productPesIds="16348"
	cloudEnvironments="public"
/>

# I cannot connect to vCenter server

## **Recommended steps**

**Error UnhandledException Internal error occured: System.IO.FileNotFoundException**

Please follow these steps to resolve the error:
1. If you are not on the latest Collector version, upgrade the Collector to the [latest version](https://docs.microsoft.com/azure/migrate/concepts-collector#how-to-upgrade-collector) and check if the issue is resolved.
2. If you already have the latest Collector version, manually install [VMware PowerCLI 6.5](https://www.powershellgallery.com/packages/VMware.PowerCLI/6.5.2.6268016) and check if the issue is resoloved.
3. If that does not work, remove VMware.Vim.dll and VimService65.dll dlls present in 'C:\Program Files\ProfilerService' folder and restart the Azure Migrate Collector service.

**Error UnableToConnectToServer**

Unable to connect to vCenter Server "Servername.com:9443" due to error: There was no endpoint listening at https://Servername.com:9443/sdk that could accept the message.

This happens when the Collector machine is unable to resolve the vCenter server name specified or the port speficified is wrong. By default, if the port is not specified, the Collector will try to connect to the port number 443.
Please follow these steps to check connection:
1. Try to ping the Servername.com from the Collector machine.
2. If step 1 fails, try to connect to the vCenter server over IP address.
3. Identify the correct port number to connect to the vCenter if vCenter server is configured with non-default port.
4. Finally check if the vCenter server is up and running.
