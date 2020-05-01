<properties
	pageTitle="Azure Backup - Backup is taking longer than expected"
	description="Azure Backup - Backup is taking longer than expected"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder="9"
	selfHelpType="generic"
	supportTopicIds="32637321"
	resourceTags="windows,linux,redhat,ubuntu"
	productPesIds="15571,15797,16470,16454,14749"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="fdee12e71-369d-4812-9400-8a81bd302190"
	ownershipId="StorageMediaEdge_Backup"
/>

# Azure Backup - Backup is taking longer than expected

## **Recommended Steps**

* Note that a first backup time **can be greater than 24 hours**, as it is proportional to the size of the source data<br>
* Subsequent (i.e. incremental or daily) backup time **can take up to 24 hours** to complete<br>
* Understand the [factors contributing to backup time](https://aka.ms/AB-AA4ecqb)<br>
* Follow [best practices](https://aka.ms/AB-AA4e56d) to optimize backup performance

## **Recommended Documents**

* [Configure Azure VMs Backup in Recovery Services vault](https://aka.ms/AB-AA4ecq2)<br>
* [Enable Backup during VM creation](https://aka.ms/AB-EnableBackupDuringVMcreation)<br>
* [Enable Backup from VM blade](https://aka.ms/AB-EnableBackupDuringVMcreation)<br>
* [Restore VM](https://aka.ms/AB-AA4e568)<br>
* [Restore files from VM backup](https://aka.ms/AB-AA4e56h)<br>
* [Restore VM to alternate location](https://aka.ms/AB-AA4e570)<br>
* [Create VM from restored disks](https://aka.ms/AB-AA4e56j)<br>
* [Configure](https://aka.ms/AB-backupReorts) and [view](https://aka.ms/View-PowerBI-Report) Backup report using Power BI<br>
* Monitor [Alerts and Jobs](https://aka.ms/Monitor-JobsAlert-RSV) through Recovery Services vault<br>
* [Configure Notifications](https://aka.ms/Configure-Notification-RSV) for backup Alerts through Recovery Services vault<br>
* [Monitor Azure Backup](https://aka.ms/Monitor-Backup-LA) and [create Alerts](https://aka.ms/Create-Alert-LA) using Log Analytics<br>
* [Stop protecting virtual machines](https://aka.ms/AB-AA4ecqs)<br>
* [Delete Backup data](https://aka.ms/AB-AA4e56f)<br>
* [Delete Recovery Services vault](https://aka.ms/AB-AA4ecq5)
