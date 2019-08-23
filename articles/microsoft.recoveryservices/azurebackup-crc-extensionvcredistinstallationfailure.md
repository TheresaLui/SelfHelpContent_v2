<properties
	pageTitle="ExtensionVCRedistInstallationFailure"
	description="ExtensionVCRedistInstallationFailure"
	infoBubbleText="Snapshot operation failed due to failure in installation of Visual C++ Redistributable for Visual Studio 2012."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	displayOrder=""
	articleId="azurebackup-crc-extensionvcredistinstallationfailure"
	diagnosticScenario="azurebackup-crc-extensionvcredistinstallationfailure"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
/>

# Error ExtensionVCRedistInstallationFailure

<!--issueDescription-->
We have identified that your backup operation failed due to an failure while installating Visual C++ Redistributable for Visual Studio 2012.
<!--/issueDescription-->

## **Recommended Step**

To resolve this issue, install [Visual C++ Redistributable for Visual Studio 2013]((https://www.microsoft.com/download/details.aspx?id=40784)). If you encounter any issue during this installation, then perform the below:

**Step 1:**

- Ensure HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\Msiserver registry key value is set to 3 and not 4 for allowing this service installation.
- Restart installation service from the elevated command prompt by running the below command:<br/>
```MSIEXEC /UNREGISTER```<br/>
```MSIEXEC /REGISTER```
	
- If issue still persist after installation then reboot the VM and retry backup operation. <br/>

**Step 2:**

- To set the Reg-key run the below command and then retry the backup operation: <br/>
```REG ADD "HKLM\SOFTWARE\Microsoft\BcdrAgentPersistentKeys" /v IsVCRedistInstalled /t REG_SZ /d True /f```
