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

This is an issue seen on Collector versions less than 1.0.9.5. If you are on a Collector version 1.0.9.2 or pre-GA versions like 1.0.8.59, you will face this issue. Follow the [link given here to the forums for a detailed answer](https://social.msdn.microsoft.com/Forums/azure/c1f59456-7ba1-45e7-9d96-bae18112fb52/azure-migrate-connect-to-vcenter-server-error?forum=AzureMigrate).

[Upgrade your Collector to fix the issue](https://aka.ms/migrate/col/checkforupdates).

**Error UnableToConnectToServer**

Unable to connect to vCenter Server "Servername.com:9443" due to error: There was no endpoint listening at https://Servername.com:9443/sdk that could accept the message.

This happens when the Collector machine is unable to resolve the vCenter server name specified or the port speficified is wrong. By default, if the port is not specified, Collector will try to connect to the port number 443.

1. Try to ping the Servername.com from the Collector machine.
2. If step 1 fails, try to connect to the vCenter server over IP address.
3. Identify the correct port number to connect to the vCenter.
4. Finally check if the vCenter server is up and running.