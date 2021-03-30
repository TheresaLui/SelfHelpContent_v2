<properties
	pageTitle="Issues in managing Azure VM backup"
	description="Issues in managing Azure VM backup"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="trinadhk"
	ms.author="trinadhk"
	displayOrder="8"
	selfHelpType="generic"
	supportTopicIds="32783170"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="ddeb7798-d489-483b-8a96-9d3ca73b456e"
	ownershipId="StorageMediaEdge_Backup"
/>

# Azure IAAS VM Backup - Manage

## **Recommended Steps**

**Backup policies and retention**

- [How do I **clean up or extend the retention period** of Recovery points?](https://docs.microsoft.com/azure/backup/backup-azure-manage-vms#manage-backup-policy-for-a-vm)<br>
- [How do I perform **multiple backups per day**? ](https://docs.microsoft.com/azure/backup/backup-azure-manage-vms#run-an-on-demand-backup)<br>
- [How can I modify the retention period?](https://docs.microsoft.com/azure/backup/backup-azure-manage-vms#manage-backup-policy-for-a-vm)
- [What happens to the existing recovery points if I change the retention policy?](https://docs.microsoft.com/azure/backup/backup-architecture#backup-policy-essentials)
- Learn more about [backup policies](https://docs.microsoft.com/azure/backup/backup-architecture#backup-policy-essentials)
- [How retention of recovery points works?](https://docs.microsoft.com/azure/backup/manage-recovery-points)
- [What happens to my existing backup when I modify the backup policy?](https://docs.microsoft.com/azure/backup/backup-architecture#impact-of-policy-change-on-recovery-points)

**Backup Reports/Alerts**<br>
- [How to **check backup data size** for backup items?](https://docs.microsoft.com/azure/backup/configure-reports)<br>
- [Configure](https://docs.microsoft.com/azure/backup/configure-reports) and [view](https://docs.microsoft.com/azure/backup/configure-reports#what-happened-to-the-power-bi-reports) Backup report using Power BI<br>
- [Why am I not receiving backup alerts?](https://docs.microsoft.com/azure/backup/backup-azure-monitoring-built-in-monitor#exceptions-when-an-alert-is-not-raised)<br>
- [Configure notifications](https://docs.microsoft.com/azure/backup/backup-azure-monitoring-built-in-monitor#notification-for-backup-alerts) for backup Alerts through Recovery Services vault <br>
- [Monitor Azure Backup](https://docs.microsoft.com/azure/backup/backup-azure-monitoring-use-azuremonitor#using-log-analytics-workspace) and [create Alerts](https://docs.microsoft.com/azure/backup/backup-azure-monitoring-use-azuremonitor#create-alerts-by-using-log-analytics) using Log Analytics<br>
- Monitor [Alerts and Jobs](https://docs.microsoft.com/azure/backup/backup-azure-monitoring-built-in-monitor#backup-jobs-in-recovery-services-vault) through Recovery Services vault<br>

**Moving resources**

- [How do I change my vault storage replication type from **GRS to LRS**?](https://docs.microsoft.com/azure/backup/backup-create-rs-vault#how-to-change-from-grs-to-lrs-after-configuring-backup)<br>
- How to move resources: Azure VM across [Resource Group](https://docs.microsoft.com/azure/backup/backup-azure-vm-backup-faq#how-do-i-move-a-vm-backed-up-by-azure-backup-to-a-different-resource-group); VMs across [Vault](https://docs.microsoft.com/azure/backup/backup-azure-move-recovery-services-vault#move-an-azure-virtual-machine-to-a-different-recovery-service-vault); Vault across [Resource Group](https://docs.microsoft.com/azure/backup/backup-azure-move-recovery-services-vault#use-azure-portal-to-move-recovery-services-vault-to-different-resource-group); Vault across [Subscription](https://docs.microsoft.com/azure/backup/backup-azure-move-recovery-services-vault#use-azure-portal-to-move-recovery-services-vault-to-a-different-subscription).<br>
- **Moving Recovery points/backup data** across Vaults/Subscription is not supported. <br>

**Backup pricing**<br>
- Understanding Azure Backup [**pricing**](https://docs.microsoft.com/azure/backup/backup-azure-vms-introduction#backup-costs) and [charges](https://azure.microsoft.com/pricing/details/backup/)<br>

## **Recommended Documents**

- [Complete list of supported and unsupported actions and scenarios and known limitations](https://docs.microsoft.com/azure/backup/backup-support-matrix-iaas) for Azure VM backup
- [Common configuration errors and how to troubleshoot them](https://docs.microsoft.com/azure/backup/backup-azure-vms-troubleshoot)
- [Troubleshooting Azure VM extension and Guest Agent issues](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout)
