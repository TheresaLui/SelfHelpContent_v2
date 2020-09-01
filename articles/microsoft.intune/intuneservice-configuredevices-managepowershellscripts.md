<properties
	pageTitle="Configure Devices - Manage PowerShell scripts"
	description="Configure Devices - Manage PowerShell scripts"
	service="microsoft.intune"
	resource="intune"
	authors="rciliax"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32599651"
	resourceTags=""
	productPesIds="15584"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="af239d24-bb78-43fe-95c3-6363435bfe3b"
	ownershipId="IntuneCxP_Intune"
/>

# Configure Devices - Manage PowerShell scripts

## **Recommended Steps**

Depending on your scenario, follow the appropriate troubleshooting steps outlined below. 

**The Intune Management Extension is not installing or downloading.**

Check and make sure that you've assigned a user group and not a device group. Devices within the group must be auto-enrolled or bulk auto-enrolled. Other enrollment types are not supported.

**PowerShell script extensions are installed, but scripts are not running or they have errors.**

* Check your logs for events relating to the script. Look for errors in the log files located in **ProgramData/Microsoft/IntuneManagementExtension/Logs**. 
* If you suspect an issue with the script you can create a test script to check that a script can run successfully. You must have access to the output path to view the test results. Create the c:\scripts directory on the client. Then use the following PowerShell script to deploy the test script:

   Start-Transcript -Path c:\scripts\ScriptProgress.log
   write-output "Script worked" | out-file c:\scripts\ScriptLog.log
   Stop-Transcript

## **Recommended documents**

* [Manage PowerShell scripts in Intune for Windows 10 devices](https://docs.microsoft.com/intune/intune-management-extension)<br>
* [Troubleshooting device profiles in Microsoft Intune](https://docs.microsoft.com/intune/device-profile-troubleshoot)<br>
* [Review Intune TechNet to find answers and solutions to common issues](https://aka.ms/intuneforums)<br>
* [Check out Service Health to see current status of the service](https://portal.office.com/AdminPortal/Home#/MessageCenter)<br>
