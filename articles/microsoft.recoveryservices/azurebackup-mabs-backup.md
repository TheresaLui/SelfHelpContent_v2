<properties
	pageTitle="Microsoft Azure Backup Server"
	description="Azure Backup server backup/register or back up a windows virtual machine"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32553284"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
	articleId="5823f408-f546-4330-b2d4-96bef885876a"
/>

# Troubleshooting Azure Backup Server failures issues?

## **Recommended Steps**
- [Ensure Microsoft Azure Recovery Services (MARS) Agent is up to date before troubleshooting further](https://go.microsoft.com/fwlink/?linkid=229525&clcid=0x409)
- [Ensure 5-10% free volume space is available on scratch folder location](https://docs.microsoft.com/azure/backup/backup-azure-file-folder-backup-faq#whats-the-minimum-size-requirement-for-the-cache-folder-br) <br>
- [**Online recovery point creation failed**](https://docs.microsoft.com/azure/backup/backup-azure-mabs-troubleshoot#backup)<br>
- [**Replica is Inconsistent**](https://docs.microsoft.com/azure/backup/backup-azure-mabs-troubleshoot#backup)<br>
- [**Invalid vault credentials provided**](https://docs.microsoft.com/azure/backup/backup-azure-mabs-troubleshoot#invalid-vault-credentials-provided)<br>
- [**The encryption passphrase stored for this computer is not correctly configured**](https://docs.microsoft.com/azure/backup/backup-azure-mabs-troubleshoot#change-passphrase)<br>
- [**Setup could not update registry metadata**](https://docs.microsoft.com/azure/backup/backup-azure-mabs-troubleshoot#setup-could-not-update-registry-metadata)<br>
- [DPM encountered error from VMware while trying to get ChangeTracking information](https://blogs.technet.microsoft.com/dpm/2017/03/29/change-block-tracking-needs-to-be-reset-if-another-backup-product-has-protected-a-vmware-vm-prior-to-dpm/)<br>

## **Recommended Documents**

For information on pre-requisites, limitations and frequently asked questions, see:<br>

- [Step by step guide to setup Azure Backup Server](https://docs.microsoft.com/azure/backup/backup-azure-microsoft-azure-backup)<br>
- [Support matrix for Microsoft Azure Backup Server](https://docs.microsoft.com/azure/backup/backup-mabs-protection-matrix)<br>
- [Pricing details](https://azure.microsoft.com/pricing/details/backup/)<br>
- [What workloads, I can protect with Azure Backup Server?](https://docs.microsoft.com/azure/backup/backup-azure-backup-server-vmware)<br>
- [How to Upgrade Backup Server to V3](https://docs.microsoft.com/azure/backup/backup-azure-microsoft-azure-backup#upgrade-mabs)<br>
- [What's new in Microsoft Azure Backup Server](https://docs.microsoft.com/azure/backup/backup-mabs-whats-new-mabss)<br>
