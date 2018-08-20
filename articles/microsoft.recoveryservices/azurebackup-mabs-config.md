<properties
	pageTitle="Microsoft Azure Backup Server"
	description="Azure Backup server backup/register or back up a windows virtual machine"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="v-bllydi"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32570754"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
/>

# Troubleshooting Azure Backup Server Configuration/Registration issues

## **Recommended steps**
- Ensure the server on which you are trying to install Azure Backup Server is not already registered with another vault <br> 
- [Push install failed? try manual install](https://aka.ms/marsmanualinstall)<br>
- If Push install fails, check if DPM agent is already present. If yes, then uninstall the agent and retry the installation<br>
- [Setup could not update registry metadata](https://docs.microsoft.com/azure/backup/backup-azure-mabs-troubleshoot#installation-issues)<br>
- [The agent operation failed because of a communication error with the DPM agent...](https://docs.microsoft.com/azure/backup/backup-azure-mabs-troubleshoot#the-agent-operation-failed-because-of-a-communication-error-with-the-dpm-agent-coordinator-service-on-the-server)<br>
- [The Microsoft Azure Recovery Service Agent was unable to connect to Microsoft Azure Backup](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot#the-microsoft-azure-recovery-service-agent-was-unable-to-connect-to-microsoft-azure-backup)<br>
- [Invalid vault credentials provided](https://docs.microsoft.com/azure/backup/backup-azure-mabs-troubleshoot#invalid-vault-credentials-provided)<br>
- [The encryption passphrase stored for this computer is not correctly configured](https://docs.microsoft.com/azure/backup/backup-azure-mabs-troubleshoot#change-passphrase)<br>


## **Recommended documents**

For information on pre-requisites, limitations and frequently asked questions, see:<br>
- [Step by step guide to setup Azure Backup Server](https://docs.microsoft.com/azure/backup/backup-azure-microsoft-azure-backup)<br>
- [Support matrix for Azure Backup Server](https://docs.microsoft.com/azure/backup/backup-mabs-protection-matrix)<br>
- [Pricing details](https://azure.microsoft.com/pricing/details/backup/)<br>
- [What workloads, I can protect with Azure Backup Server?](https://docs.microsoft.com/azure/backup/backup-azure-backup-server-vmware)<br>
- [How to Upgrade Backup Server to v2](https://docs.microsoft.com/azure/backup/backup-mabs-upgrade-to-v2#upgrade-backup-server-to-v2)<br>
