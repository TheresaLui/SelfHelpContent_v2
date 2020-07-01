<properties
	pageTitle="Troubleshooting Azure File Sync - Tiering Policy"
	description="Troubleshooting Azure File Sync - Tiering Policy"
	service="microsoft.storage"
	resource="storageaccounts"
	authors="jeffpatt24"
	ms.author="jeffpatt"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32675714"
	resourceTags=""
	productPesIds="16460"
	cloudEnvironments="public,MoonCake,FairFax,BlackForest, usnat, ussec"
	articleId="812e832a-8f48-4526-bb3c-29760c43c854"
	ownershipId="StorageMediaEdge_StorageFiles"
/>

# Troubleshooting Azure File Sync - Tiering policy not met

## **Recommended Documents**

**Cloud Tiering Configuration**

- [How does the volume free space tiering policy work?](https://docs.microsoft.com/azure/storage/files/storage-sync-cloud-tiering#how-does-the-volume-free-space-tiering-policy-work)<br>
- [How does the volume free space tiering policy work with regards to new server endpoints?](https://docs.microsoft.com/azure/storage/files/storage-sync-cloud-tiering#how-does-the-volume-free-space-tiering-policy-work-with-regards-to-new-server-endpoints)<br>
- [How do I determine the appropriate amount of volume free space?](https://docs.microsoft.com/azure/storage/files/storage-sync-cloud-tiering#how-do-i-determine-the-appropriate-amount-of-volume-free-space)<br>
- [How is volume free space interpreted when I have multiple server endpoints on a volume?](https://docs.microsoft.com/azure/storage/files/storage-sync-cloud-tiering#how-is-volume-free-space-interpreted-when-i-have-multiple-server-endpoints-on-a-volume)<br>
- [How does the date tiering policy work in conjunction with the volume free space tiering policy?](https://docs.microsoft.com/azure/storage/files/storage-sync-cloud-tiering#how-does-the-date-tiering-policy-work-in-conjunction-with-the-volume-free-space-tiering-policy)

**Cloud Tiering Failures**

- [Tiered files are not accessible on the server after deleting a server endpoint](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#tiered-files-are-not-accessible-on-the-server-after-deleting-a-server-endpoint)<br>
- [Troubleshoot files that fail to be recalled](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#how-to-troubleshoot-files-that-fail-to-be-recalled)<br>
- [Troubleshoot files that fail to tier](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#how-to-troubleshoot-files-that-fail-to-tier)<br>
- [Troubleshoot files unexpectedly recalled on a server](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#how-to-troubleshoot-files-unexpectedly-recalled-on-a-server)

**Cloud Tiering Monitoring**

- [Monitor Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-monitoring)<br>
- [How to monitor tiering activity on a server](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#how-to-monitor-tiering-activity-on-a-server)<br>
- [How to monitor recall activity on a server](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#how-to-monitor-recall-activity-on-a-server)<br>
- [How do I tell whether a file has been tiered?](https://docs.microsoft.com/azure/storage/files/storage-sync-cloud-tiering#is-my-file-tiered)
