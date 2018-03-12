<properties
	pageTitle="Site Recovery (VMware to Azure) Advisory"
	description="Site Recovery (VMware to Azure) Advisory"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="asgang"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32536384"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
/>

# Advisory questions for Enable Replication

## **Recommended Steps**
**How to Replicate on-premises VMware VMs to Azure?**<br>
- How to [Set up the source/VMWare environment](https://docs.microsoft.com/azure/site-recovery/site-recovery-set-up-vmware-to-azure)
and [prepare the target/Azure environment?](https://docs.microsoft.com/azure/site-recovery/site-recovery-prepare-target-vmware-to-azure) <br>
- What are the [**supported/not-supported configurations**](https://docs.microsoft.com/azure/site-recovery/site-recovery-support-matrix-to-azure) for VMware to  Azure replicaton?<br>
- What are the [**pre-checks**](https://docs.microsoft.com/azure/site-recovery/vmware-walkthrough-prerequisites)  required for VMware to Azure replication?<br>
- What [**workloads**](https://docs.microsoft.com/azure/site-recovery/site-recovery-workload#workload-summary) can I protect with Site Recovery?<br>
- [What charges do I incur while using Azure Site Recovery?](https://docs.microsoft.com/azure/site-recovery/site-recovery-faq#pricing) <br>
- Ensure you run [**Deployment planner**](https://docs.microsoft.com/azure/site-recovery/site-recovery-deployment-planner) for capacity planning to replicate VMware VMs to Azure<br>

**Mobility Service agents can be deployed on source VM** using one of below methods:<br>
- Manually install Agent using: [**GUI**](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-install-mob-svc#install-mobility-service-manually-by-using-the-gui), [**Command prompt**](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-install-mob-svc#install-mobility-service-manually-at-a-command-prompt), [**Software deployment tools**](https://docs.microsoft.com/azure/site-recovery/site-recovery-install-mobility-service-using-sccm), [**Azure Automation DSC**](https://docs.microsoft.com/azure/site-recovery/site-recovery-automate-mobility-service-install)<br>
- [Push installation of mobility agents from Azure](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-install-mob-svc#install-mobility-service-by-push-installation-from-azure-site-recovery) - must meet below prerequisites before you click 'Enable replication'. <br>
  - [Push installation prerequisites for Windows machine](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-install-mob-svc#prepare-for-a-push-installation-on-a-windows-computer) <br>
  - [Push installation prerequisites for Linux machine](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-install-mob-svc#prepare-for-a-push-installation-on-a-linux-server) <br>
