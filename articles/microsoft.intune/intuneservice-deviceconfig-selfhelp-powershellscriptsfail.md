<properties
	pageTitle="PowerShell script extensions are installed, but scripts are not running or they have errors."
	description="PowerShell script extensions are installed, but scripts are not running or they have errors."
	service="microsoft.intune"
	resource="intune"
	authors="mackie1604"
	displayOrder="7"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="deviceconfiguration_selfhelp"
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="7312f696-2f91-4f94-87e1-63e5fa87a4d7"
	ownershipId="IntuneCxP_Intune"
/>

# PowerShell script extensions are installed, but scripts are not running or they have errors.

## **Recommended steps**

Follow one or both of these suggested steps to help pinpoint the cause of error.

* Check your logs for events relating to the script. Look for errors in the log files located in **ProgramData/Microsoft/IntuneManagementExtension/Logs**. 
* If you suspect an issue with the script you can create a test script to check that a script can run successfully. You must have access to the output path to view the test results. Create the c:\scripts directory on the client. Then use the following PowerShell script to deploy the test script:

   Start-Transcript -Path c:\scripts\ScriptProgress.log
   write-output "Script worked" | out-file c:\scripts\ScriptLog.log
   Stop-Transcript