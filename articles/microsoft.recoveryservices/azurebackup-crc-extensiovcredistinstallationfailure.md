<properties
	pageTitle="extensiovcredistinstallationfailure"
	description="extensiovcredistinstallationfailure"
	infoBubbleText="Snapshot operation failed due to failure in installation of Visual C++ Redistributable for Visual Studio 2012."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathv"
	ms.author="srinathv"
	articleId="azurebackup-crc-extensiovcredistinstallationfailure"
	diagnosticScenario="azurebackup-crc-extensiovcredistinstallationfailure"
	selfHelpType="diagnostics"
	supportTopicIds=""
	productPesIds="15207"
	cloudEnvironments="public"
/>

# ExtensionVCRedistInstallationFailure

<!--issueDescription-->
## **Visual C++ redistributable required to load the Backup extension failed resulting in backup operation failure.**
<!--/issueDescription-->

## **Recommended Steps**
Installation of Visual C++ Redistributable for Visual Studio failed, this is required to load the Backup Extension to perform the backup operation. To resolve this issue perform the below:

**Step 1**: To install Visual C++ Redistributable for Visual Studio 2013.

* Go to C:\Packages\Plugins\Microsoft.Azure.RecoveryServices.VMSnapshot\<LatestVersion> folder and run **vcredist2013_x64** file or download the installer from [here](https://www.microsoft.com/download/details.aspx?id=40784). Retry backup operation.
* If you encounter an issue during installation, then ensure HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\Msiserver registry key value is set to **3** and not **4** for allowing this service installation.
* Restart installation service from the elevated command prompt by running the below command:

 	`MSIEXEC /UNREGISTER`
	`MSIEXEC /REGISTER`

* Reboot the VM and retry backup operation.

**Step 2**: If **Step 1** fails, then perform the below:

Run the below command from the elevated command prompt to set the **Reg-key** and then trigger the backup operation.

` REG ADD "HKLM\SOFTWARE\Microsoft\BcdrAgentPersistentKeys" /v IsVCRedistInstalled /t REG_SZ /d True /f `

