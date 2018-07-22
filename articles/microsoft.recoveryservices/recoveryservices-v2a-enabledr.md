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
	productPesIds="16370"
	cloudEnvironments="public"
/>

# Enable Protection - VMware/Physical to Azure

## **Recommended documents**
* Troubleshoot [Enable replication issues](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-protection-troubleshoot/) <br>
* Ensure push installation prerequisites for [Windows](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-install-mob-svc#prepare-for-a-push-installation-on-a-windows-computer) and [Linux](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-install-mob-svc#prepare-for-a-push-installation-on-a-linux-server) are met <br>
* Troubleshoot common [Mobility service push install failures](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-push-install-error-codes) <br>
* Mobility service push install not successful? Try the [Manual installation](https://docs.microsoft.com/azure/site-recovery/vmware-azure-install-mobility-service#prerequisites) of agents </br>
* Troubleshoot [Initial replication issues](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-protection-troubleshoot/) <br>
* [Enable replication failing due to stale entries from previous installation?](https://social.technet.microsoft.com/wiki/contents/articles/32026.asr-vmware-to-azure-how-to-cleanup-duplicatestale-entries.aspx) <br>
* [Ensure ASR agents are up to date](https://social.technet.microsoft.com/wiki/contents/articles/38544.azure-site-recovery-service-updates.aspx) <br>
* **Protection could not enabled**  error codes:<br>[Error 95105 (EP0856)](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-push-install-error-codes#error-95105---protection-could-not-be-enabled-ep0856)<br>[Error 95107 (EP0858)](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-push-install-error-codes#error-95107---protection-could-not-be-enabled-ep0858)<br>[Error 95117 (EP0865)](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-push-install-error-codes#error-95117---protection-could-not-be-enabled-ep0865)<br>[Error 95103  (EP0854)](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-push-install-error-codes#error-95103---protection-could-not-be-enabled-ep0854)<br>[Error 95213  (EP0874)](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-push-install-error-codes#error-95213---protection-could-not-be-enabled-ep0874)<br>[Error 95108 (EP0859)](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-push-install-error-codes#error-95108---protection-could-not-be-enabled-ep0859)<br>[Error 95265 (EP0902)](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-push-install-error-codes#error-95265---protection-could-not-be-enabled-ep0902)<br>[Error 95224  (EP0883)](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-push-install-error-codes#error-95224---protection-could-not-be-enabled-ep0883)<br>
