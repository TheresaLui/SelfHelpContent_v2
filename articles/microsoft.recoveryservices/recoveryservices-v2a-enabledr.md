<properties
	pageTitle="Site Recovery (VMware to Azure)/Enable Protection"
	description="Site Recovery (VMware to Azure)/Common issues during Enable Protection"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="Rajeswari-Mamilla"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32536405"
	resourceTags=""
	productPesIds="16370"
	cloudEnvironments="public"
/>

# Enable Protection - VMware/Physical to Azure

## **Recommended documents**

- If you have received an error stating that *Enable Replication failed* due to **push installation of mobility service failure**, refer to the following links of troubleshooting steps for the most common causes: <br>
	-	[Credential/privilege errors](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#credentials-check-errorid-95107--95108) <br>
	-	[Connectivity errors](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#connectivity-check-errorid-95117--97118) <br>
	-	[File sharing, printer/WMI configuration errors](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#file-and-printer-sharing-services-check-errorid-95105--95106) <br>
	-	[Unsupported operating system errors](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#unsupported-operating-systems) <br>
	-	[VSS installation failures](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#vss-installation-failures)

- To quickly **unblock Mobility Service push installation failure**, ensure push installation prerequisites for [Windows](https://docs.microsoft.com/azure/site-recovery/vmware-azure-install-mobility-service#prepare-for-a-push-installation-on-a-windows-computer) and [Linux](https://docs.microsoft.com/azure/site-recovery/vmware-azure-install-mobility-service#prepare-for-a-push-installation-on-a-linux-server) are met. <br>
- Replication issues due to high churn? Read the [capacity planning document](https://docs.microsoft.com/azure/site-recovery/site-recovery-plan-capacity-vmware#capacity-considerations) to verify your configurations. <br>
- Troubleshoot [initial replication issues](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-replication).<br>
- Our latest release contains the fix to known issues. [Upgrade to the latest versions to fix them immediately](https://docs.microsoft.com/azure/site-recovery/vmware-physical-azure-support-matrix#download-latest-azure-site-recovery-components). <br>
- Enable replication failing due to stale entries from previous installation? Follow this [link](https://social.technet.microsoft.com/wiki/contents/articles/32026.asr-vmware-to-azure-how-to-cleanup-duplicatestale-entries.aspx) to resolve the issue. <br>
