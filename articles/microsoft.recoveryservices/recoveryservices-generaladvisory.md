<properties
	pageTitle="Site Recovery/General Guidance or Advisory"
	description="General advisory questions"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="asgang,genlin"
	ms.author="asgang,genli"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32452761"
	resourceTags=""
	productPesIds="16370"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="d335c49e-d501-4d26-a3b5-e7cc63c648fa"
	ownershipId="Compute_SiteRecovery"
/>

# Azure Site Recovery Advisory Queries

**Prerequisites**

- Supported scenarios and requirements for setting up disaster recovery to Azure: 

    - [Azure VMs to Azure](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-support-matrix)
    - [VMware VMs to Azure](https://docs.microsoft.com/azure/site-recovery/vmware-physical-azure-support-matrix)
    - [Hyper-V VMs to Azure](https://docs.microsoft.com/azure/site-recovery/hyper-v-azure-support-matrix)
    - [Physical servers to Azure](https://docs.microsoft.com/azure/site-recovery/vmware-physical-azure-support-matrix)

- Run [Deployment Planner](https://docs.microsoft.com/azure/site-recovery/hyper-v-deployment-planner-overview) for capacity planning, and check whether your network bandwidth and storage allocations are sufficient for the amount of churn in your VMs
- [Azure Site Recovery pricing](https://docs.microsoft.com/azure/site-recovery/site-recovery-faq#pricing)

## **Recommended Documents**

### Azure VMs to Azure

**Tutorials**

1. [Set up disaster recovery for Azure VMs to a secondary Azure region](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-tutorial-enable-replication)
2. [Run a disaster recovery drill for Azure VMs to a secondary Azure region](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-tutorial-dr-drill)
3. [Failover and failback Azure VMs between Azure regions](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-tutorial-failover-failback)

**Common Issues**

- [Unable to see Azure VM for selection in "Enable replication"](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-troubleshoot-errors#unable-to-see-the-azure-vm-for-selection-in-enable-replication)
- [Unable to replicate because of connectivity issues (Error code 151037 or 151072)](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-troubleshoot-errors#outbound-connectivity-for-site-recovery-urls-or-ip-ranges-error-code-151037-or-151072)
- [How to troubleshoot RDP connection to Windows VM](https://docs.microsoft.com/azure/virtual-machines/windows/troubleshoot-rdp-connection)

**FAQ**

- [Frequently asked questions](https://docs.microsoft.com//azure/site-recovery/azure-to-azure-common-questions)
- [How to retain fixed IP address after failover](https://docs.microsoft.com/azure/site-recovery/site-recovery-retain-ip-azure-vm-failover)

### VMware VMs to Azure

**Tutorials**

1. [Prepare Azure resources for disaster recovery](https://docs.microsoft.com/azure/site-recovery/tutorial-prepare-azure)
2. [Prepare on-premises VMware servers for disaster recovery to Azure](https://docs.microsoft.com/azure/site-recovery/vmware-azure-tutorial-prepare-on-premises)
3. [Set up replication to Azure for on-premises VMware VMs](https://docs.microsoft.com/azure/site-recovery/vmware-azure-tutorial)
4. [Run a disaster recovery drill to Azure](https://docs.microsoft.com/azure/site-recovery/tutorial-dr-drill-azure)
5. [Failover and failback VMware VMs replicated to Azure](https://docs.microsoft.com/azure/site-recovery/vmware-azure-tutorial-failover-failback)

**Common Issues**

Mobility service installation errors:

- [Credential/privilege errors](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#credentials-check-errorid-95107--95108)
- [Connectivity errors](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#connectivity-check-errorid-95117--97118)
- [File sharing, printer/WMI configuration errors](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#file-and-printer-sharing-services-check-errorid-95105--95106)
- [Unsupported operating system errors](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#unsupported-operating-systems)
- [VSS installation failures](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#vss-installation-failures)

**FAQ**

- Install new instance of [Configuration Server using OVF template]( https://docs.microsoft.com/azure/site-recovery/tutorial-vmware-to-azure#download-the-vm-template)
- [Video: Watch step-by-step installation of Configuration Server using OVF template](https://azure.microsoft.com/blog/announcing-a-new-simplified-onboarding-experience-for-azure-site-recovery-vmware-to-azure/)
- Install new instance of [Configuration Server using unified setup](https://docs.microsoft.com/azure/site-recovery/physical-manage-configuration-server#download-the-latest-installation-file)
- [Upgrading existing instance of Configuration Server](https://docs.microsoft.com/azure/site-recovery/physical-manage-configuration-server#upgrade-a-configuration-server)

### For Hyper-V to Azure

**Tutorials**

1. [Prepare Azure resources for disaster recovery of Hyper-V VMs](https://docs.microsoft.com/azure/site-recovery/tutorial-prepare-azure) 
2. [Prepare on-premises Hyper-V servers for disaster recovery to Azure](https://docs.microsoft.com/azure/site-recovery/hyper-v-prepare-on-premises-tutorial)
3. [Set up replication for Hyper-V VMs](https://docs.microsoft.com/azure/site-recovery/hyper-v-azure-tutorial) or [Hyper-V VMs in VMM clouds](https://docs.microsoft.com/azure/site-recovery/hyper-v-vmm-azure-tutorial)
4. [Run a disaster recovery drill to Azure](https://docs.microsoft.com/azure/site-recovery/tutorial-dr-drill-azure)
5. [Failover and failback Hyper-V VMs replicated to Azure](https://docs.microsoft.com/azure/site-recovery/hyper-v-azure-failover-failback-tutorial)

**FAQ**

- [Common questions - Hyper-V to Azure disaster recovery](https://docs.microsoft.com/azure/site-recovery/hyper-v-azure-common-questions)
- [Hyper-V to Azure disaster recovery architecture](https://docs.microsoft.com/azure/site-recovery/hyper-v-azure-architecture)

###  Physical servers to Azure

- [Prepare Azure resources for disaster recovery of on-premises machines](https://docs.microsoft.com/azure/site-recovery/tutorial-prepare-azure)
- [Migrate on-premises machines to Azure](https://docs.microsoft.com/azure/site-recovery/migrate-tutorial-on-premises-azure)
- [Migrate servers running Windows Server 2008 to Azure](https://docs.microsoft.com/azure/site-recovery/migrate-tutorial-windows-server-2008)
- [Physical server to Azure disaster recovery architecture](https://docs.microsoft.com/azure/site-recovery/physical-azure-architecture)

