<properties
	pageTitle="Check if you can remove old agent version"
	description="Check if you can remove old agent version"
	service="microsoft.storage"
	resource="storageAccounts"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds="32675708"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="58bc3773-ce7e-46d4-b55c-2033845b109d"
	ownershipId="StorageMediaEdge_StorageFiles"
/>

# How to remove old agent version

1. Proceed by uninstalling the old version and then attempting to install the new version.
2. Open a PowerShell admin command prompt
3. Run the powershell command to get the cached msi installer for Storage Sync Agent
4. Run msiexec to perform the uninstall and pass in the msi path from the powershell variable. 

**This will cause a server reboot!**

~~~powershell

$FileSyncAgent = Get-WMIObject -Class Win32_Product | Where-Object {$_.Name -Match "Storage Sync Agent"} | Select LocalPackage

msiexec /qn /x $FileSyncAgent.LocalPackage

~~~

5. Once the server comes back up, run the StorageSyncAgent msi packaged you downloaded from the link below

## **Recommended Documents**

1. [Agent Installer](https://www.microsoft.com/en-us/download/details.aspx?id=57159)
