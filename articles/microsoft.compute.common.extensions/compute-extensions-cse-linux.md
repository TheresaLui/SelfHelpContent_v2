<properties
	pageTitle="Azure Custom Script (CSE) extension issue"
	description="Azure Custom Script (CSE) extension issue"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="ScottAzure"
	ms.author="scotro"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32628256"
	resourceTags=""
	productPesIds="15797,15571,16454,16470"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="0f978043-20db-48ba-a5f7-e75b32083c75"
	ownershipId="Compute_VirtualMachines"
/>

# Azure Custom Script (CSE) extension issue

4 out of 5 customers resolved their extension issue using the guides listed below.<br>

A new version of Custom Script Extension is available at [GitHub CSE for Linux](https://github.com/Azure/custom-script-extension-linux). The new v2.0 version offers better reliability and wider Linux distro support.<br>

Please consider switching your new deployments to use the new version (Microsoft.Azure.Extensions.CustomScript) instead. The new version is intended to be a drop-in replacement. Therefore, the migration is as easy as changing the name and version, you do not need to change your extension configuration.<br>

## **Recommended Steps**

Review the following [*Tips and Tricks*](https://docs.microsoft.com/azure/virtual-machines/extensions/custom-script-windows#tips-and-tricks):

* The highest failure rate for this extension is due to syntax errors in the script, test the script runs without error, and also put in additional logging into the script to make it easier to find where it failed
* Write scripts that are idempotent, so if they get run again more than once accidentally, it will not cause system changes
* Ensure the scripts don't require user input when they run
* There's 90 minutes allowed for the script to run, anything longer will result in a failed provision of the extension
* Don't put reboots inside the script, this action will cause issues with other extensions that are being installed. Post reboot, the extension won't continue after the restart.<br>
* If you have a script that will cause a reboot, then install applications and run scripts etc. You can schedule the reboot using a Windows Scheduled Task, or using tools such as DSC, or Chef, Puppet extensions.<br>
* The extension will only run a script once, if you want to run a script on every boot, then you need to use the extension to create a Windows Scheduled Task
* If you want to schedule when a script will run, you should use the extension to create a Windows Scheduled Task
* When the script is running, you will only see a 'transitioning' extension status from the Azure portal or CLI. If you want more frequent status updates of a running script, you'll need to create your own solution.<br>
* Custom Script extension does not natively support proxy servers, however, you can use a file transfer tool that supports proxy servers within your script, such as Curl
* Be aware of non-default directory locations that your scripts or commands may rely on, have logic to handle this situation

## **Recommended Documents**

* [Overview of Azure Custom Script Extension for Linux](https://docs.microsoft.com/azure/virtual-machines/extensions/custom-script-linux)<br>
* [Troubleshoot Azure Custom Script Extension](https://docs.microsoft.com/azure/virtual-machines/extensions/custom-script-linux#troubleshooting)<br>
* [FAQ for common issues and tips](https://docs.microsoft.com/azure/virtual-machines/extensions/custom-script-linux#tips-and-tricks)<br>
* [Understanding the schema and parameters](https://docs.microsoft.com/azure/virtual-machines/extensions/custom-script-linux#extension-schema)<br>
* [Overview of Azure Extensions for Windows](https://docs.microsoft.com/azure/virtual-machines/extensions/features-linux)<br>
* [How to configure Extensions via the Azure Portal](https://docs.microsoft.com/azure/virtual-machines/extensions/features-linux#azure-portal)<br>
* [General troubleshooting steps for extensions](https://docs.microsoft.com/azure/virtual-machines/extensions/troubleshoot)
