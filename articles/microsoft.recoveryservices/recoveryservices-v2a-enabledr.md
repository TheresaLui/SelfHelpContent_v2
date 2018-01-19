<properties
	pageTitle="Site Recovery (VMware to Azure)/Enable Protection"
	description="Site Recovery (VMware to Azure)/Common issues during Enable Protection"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="asgang"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32536405"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
/>

# Can't Enable Replication? Initial Replication Failing?

## **Recommended Steps**
- [**Can't Enable Replication? Initial Replication Failing?**](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-protection-troubleshoot/) <br>
- **Common Mobility Service push installation errors**
  - [Error 78007 - The requested operation could not be completed](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-push-install-error-codes) <br>
  - **Protection could not enabled**  error codes: [Error 95105 (EP0856)](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-push-install-error-codes#error-95105---protection-could-not-be-enabled-ep0856), [Error 95107 (EP0858)](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-push-install-error-codes#error-95107---protection-could-not-be-enabled-ep0858), [Error 95117 (EP0865)](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-push-install-error-codes#error-95117---protection-could-not-be-enabled-ep0865), [Error 95103  (EP0854)](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-push-install-error-codes#error-95103---protection-could-not-be-enabled-ep0854), [Error 95213  (EP0874)](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-push-install-error-codes#error-95213---protection-could-not-be-enabled-ep0874), [Error 95108 (EP0859)](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-push-install-error-codes#error-95108---protection-could-not-be-enabled-ep0859), [Error 95265 (EP0902)](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-push-install-error-codes#error-95265---protection-could-not-be-enabled-ep0902) and [Error 95224  (EP0883)](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-push-install-error-codes#error-95224---protection-could-not-be-enabled-ep0883). <br>
- [Enable replication failing due to stale entries from previous installation](https://social.technet.microsoft.com/wiki/contents/articles/32026.asr-vmware-to-azure-how-to-cleanup-duplicatestale-entries.aspx) <br>
- [Ensure your agents are up to date](https://social.technet.microsoft.com/wiki/contents/articles/38544.azure-site-recovery-service-updates.aspx) <br>

## **Recommended Documents**

**How to Replicate on-premises VMware VMs to Azure?**
- How to [Set up the source/VMWare environment](https://docs.microsoft.com/azure/site-recovery/site-recovery-set-up-vmware-to-azure)
and [prepare the target/Azure environment ](https://docs.microsoft.com/azure/site-recovery/site-recovery-prepare-target-vmware-to-azure) <br>
- [What are the supported/not-supported configurations for VMware to  Azure replicaton?](https://docs.microsoft.com/azure/site-recovery/site-recovery-support-matrix-to-azure) <br>
- [What are the pre-checks required for VMware to Azure replication](https://docs.microsoft.com/azure/site-recovery/vmware-walkthrough-prerequisites) <br>
- [What workloads can I protect with Site Recovery?](https://docs.microsoft.com/azure/site-recovery/site-recovery-workload#workload-summary) <br>
- [What charges do I incur while using Azure Site Recovery?](https://docs.microsoft.com/azure/site-recovery/site-recovery-faq#pricing) <br>
- [Deployment planner for capacity planning to replicate VMware VMs to Azure](https://docs.microsoft.com/azure/site-recovery/site-recovery-deployment-planner) <br>


**Mobility Service agents can be deployed on source VM** using one of below methods:
- [Manual installation of Agent using the GUI](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-install-mob-svc#install-mobility-service-manually-by-using-the-gui) <br>
- [Manual Installation of Agent using the command prompt](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-install-mob-svc#install-mobility-service-manually-at-a-command-prompt) <br>
- [Deploying agent using Software deployment tools](https://docs.microsoft.com/azure/site-recovery/site-recovery-install-mobility-service-using-sccm) <br>
- [Deploying agent using Azure Automation DSC](https://docs.microsoft.com/azure/site-recovery/site-recovery-automate-mobility-service-install) <br>
- [Push installation of mobility agents from Azure](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-install-mob-svc#install-mobility-service-by-push-installation-from-azure-site-recovery) - For push installation of Mobility agents from azure portal to succeed, ensure these prerequisites are met before you click 'Enable replication'. <br>
  - [Push installation prerequisites for Windows machine](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-install-mob-svc#prepare-for-a-push-installation-on-a-windows-computer) <br>
  - [Push installation prerequisites for Linux machine](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-install-mob-svc#prepare-for-a-push-installation-on-a-linux-server) <br>
