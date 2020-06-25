<properties
	pageTitle="How to upgrade or install File Sync agent"
	description="How to upgrade or install File Sync agent"
	service="microsoft.storage"
	resource="storageAccounts"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="e83cca54-8186-40b4-879d-85aed96b335f"
	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# How to upgrade or install File Sync agent

Go to Apps and features, look for Storage Sync Agent. If not found or the version is older or equal to 3.1. Uninstall older File Sync agent and install then install new agent.

1. [Install new file sync agent](https://support.microsoft.com/en-us/help/4341442/general-availability-release-for-azure-file-sync-agent-july-2018)
2. If the GA agent is installed but not the newest agent
    1. Upgrade the Azure File Sync.
    2. Update File sync Agent from Microsoft Update:
      1. For Server 2016: Start > Settings > Update & Security > Check online for updates > Install Now
	  2. For Server 2012 R2: Start > Control Panel > Windows Update > Check for Updates > Important updates are available > Install
	  3. Or Manually download the update from [Manual Download ](https://docs.microsoft.com/en-us/azure/storage/files/storage-files-release-notes)or perform a silent installation for a new agent installation
3. Run the following command at an elevated command prompt:

~~~shell

msiexec /i packagename.msi /qb /l*v AFSInstaller.log

~~~

4. For example, to install the Azure File Sync agent for Windows Server 2016, run the following command:

~~~shell

msiexec /i StorageSyncAgent.msi /qb /l*v AFSInstaller.log

~~~