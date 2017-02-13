<properties
	pageTitle="Which Azure Backup components should I use"
	description="Which Azure Backup components should I use"
	service="microsoft.storage"
	resource="storageaccounts"
	authors="passaree"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32551650"
	resourceTags=""
	productPesIds="15629"
	cloudEnvironments="public"
/>

# Which Azure Backup components should I use
If you aren't sure which Azure Backup component works for your needs, see the following table for information about what you can protect with each component. The Azure portal provides a wizard, which is built into the portal, to guide you through choosing the component to download and deploy. The wizard, which is part of the Recovery Services vault creation, leads you through the steps for selecting a backup goal, and choosing the data or application to protect.

| Component | Benefits | Limits | What is protected? | Where are backups stored? |
| --- | --- | --- | --- | --- |
| Azure Backup (MARS) agent |<li>Back up files and folders on physical or virtual Windows OS (VMs can be on-premises or in Azure)<li>No separate backup server required. |<li>Backup 3x per day <li>Not application aware; file, folder, and volume-level restore only, <li>  No support for Linux. |<li>Files, <li>Folders |Azure Backup vault |
| System Center DPM |<li>Application-aware snapshots (VSS)<li>Full flexibility for when to take backups<li>Recovery granularity (all)<li>Can use Azure Backup vault<li>Linux support on Hyper-V and VMware VMs <li>Back up and restore VMware VMs using DPM 2012 R2 |Cannot back up Oracle workload.|<li>Files, <li>Folders,<li> Volumes, <li>VMs,<li> Applications,<li> Workloads |<li>Azure Backup vault,<li> Locally attached disk,<li>  Tape (on-premises only) |
| Azure Backup Server |<li>App aware snapshots (VSS)<li>Full flexibility for when to take backups<li>Recovery granularity (all)<li>Can use Azure Backup vault<li>Linux support on Hyper-V and VMware VMs<li>Back up and restore VMware VMs <li>Does not require a System Center license |<li>Cannot back up Oracle workload.<li>Always requires live Azure subscription<li>No support for tape backup |<li>Files, <li>Folders,<li> Volumes, <li>VMs,<li> Applications,<li> Workloads |<li>Azure Backup vault,<li> Locally attached disk |
| Azure IaaS VM Backup |<li>Native backups for Windows/Linux<li>No specific agent installation required<li>Fabric-level backup with no backup infrastructure needed |<li>Back up VMs once-a-day <li>Restore VMs only at disk level<li>Cannot back up on-premises |<li>VMs, <li>All disks (using PowerShell) |<p>Azure Backup vault</p> |

## **Recommended documents**
- [Azure Backup](https://docs.microsoft.com/azure/backup/backup-introduction-to-azure-backup)<br>
- [Snapshot of a Blob](https://msdn.microsoft.com/library/azure/hh488361.aspx)<br>
- [Back up Files and Folders](https://docs.microsoft.com/azure/backup/backup-try-azure-backup-in-10-mins)
- [Backup Azure Virtual Machines](https://docs.microsoft.com/azure/backup/backup-azure-vms-first-look-arm)

For details about protecting other workloads, try one of these articles:
- [SQL Server Backup and Restore with Microsoft Azure Blob Storage Service](https://msdn.microsoft.com/library/jj919148.aspx)
- [Back up your Windows Server](https://docs.microsoft.com/azure/backup/backup-configure-vault)
- [Back up application workloads](https://docs.microsoft.com/azure/backup/backup-azure-microsoft-azure-backup)
- [Backup Azure IaaS VMs](https://docs.microsoft.com/azure/backup/backup-azure-vms-prepare)
