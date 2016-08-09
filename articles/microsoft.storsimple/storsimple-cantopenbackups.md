<properties
	pageTitle="I can’t open the backups in .backups folder."
	description="I can’t open the backups in .backups folder."
	service="microsoft.storsimple"
	resource="managers"
	authors="anbacker"
	displayOrder="7"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
/>

# I can’t open the backups in .backups folder.
If you cannot open the backups in the .backups folder, do the following.


## **Recommended steps**
1. In the local web UI of the virtual array, go to Troubleshooting > Diagnostic tests and click Run diagnostic tests. Resolve any reported issues.
2. Confirm that you have permissions to the folder that you are trying to access using File Explorer. Right click on the folder name and go to **Properties** > **Security** to view the permissions.
3. If there are more than 5 backups in the .backups folder, there is a transient cleanup issue with the device. This will resolve itself in a few minutes. Retry opening the folder after you see only 5 remaining folders.


## **Recommended documents**
[Troubleshoot via the local web UI](https://aka.ms/storsimple-troubleshoot-diagnostics)
