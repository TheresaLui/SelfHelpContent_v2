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
## **Visual C++ redistributable required to load the Backup extension failed resulting in backup operation failure**
<!--/issueDescription-->

## **Recommended Steps**

Installation of Visual C++ Redistributable for Visual Studio failed. It is required to load the Backup Extension to perform the backup operation. To resolve this issue:

* Go to the `C:\Packages\Plugins\Microsoft.Azure.RecoveryServices.VMSnapshot\<LatestVersion>` folder and run the **vcredist2013_x64** file, or [download and run the installer](https://www.microsoft.com/download/details.aspx?id=40784)
* Retry backup operation
* If you encounter an issue during installation, ensure `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\Msiserver` registry key value is set to **3** and not **4** for allowing this service installation
* Restart installation service from the elevated command prompt by running the below command:

```
 	MSIEXEC /UNREGISTER
	MSIEXEC /REGISTER
```

* Reboot the VM and retry backup operation

If the above steps fail, do the steps below:

* Run the below command from the elevated command prompt to set the **Reg-key** and trigger the backup operation:

` REG ADD "HKLM\SOFTWARE\Microsoft\BcdrAgentPersistentKeys" /v IsVCRedistInstalled /t REG_SZ /d True /f `

