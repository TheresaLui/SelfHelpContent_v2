<properties
	pageTitle="Site Recovery (VMware to Azure)/Enable Protection"
	description="Site Recovery (VMware to Azure)/Common issues during Enable Protection"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="asgang"
	ms.author="asgang"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32680607"
	resourceTags=""
	productPesIds="16370"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="33a7ea22-165b-43aa-9e6e-e86009667a6b"
	ownershipId="Compute_SiteRecovery"
/>

# Enable Protection - VMware/Physical to Azure

## **Recommended Documents**

### Getting started

* **[Planning]** Trying to identify Site Recovery resources required to protect your workload? Run our [deployment planner tool](https://docs.microsoft.com/azure/site-recovery/site-recovery-deployment-planner) to obtain customized guidance on requirements, cost estimates & supported configurations.
* **Not able to find/select virtual machine on Azure portal** during Enable Replication? Click [here](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-replication#step-3-troubleshoot-source-machines-that-arent-available-for-replication) to resolve.
* Refer to the FAQ on Azure Site Recovery [here](https://docs.microsoft.com/azure/site-recovery/vmware-azure-common-questions)
* Want to protect **application workloads (say Active Directory, SQL server etc.,)** through site recovery? **Learn [more](https://docs.microsoft.com/azure/site-recovery/site-recovery-workload)** 
* **[Anti-virus]** [Manage Site Recovery folders](https://docs.microsoft.com/azure/site-recovery/vmware-azure-set-up-source#azure-site-recovery-folder-exclusions-from-antivirus-program) from your anti-virus software to ensure smooth replication

### Networking/connectivity

* Ensure that all URLs mentioned [here](https://docs.microsoft.com/azure/site-recovery/vmware-azure-deploy-configuration-server#prerequisites) are allowed on configuration server directly or via proxy for successful replication
* vCenter connectivity/discovery failure? Follow the guidelines given [here](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-configuration-server#vcenter-discovery-failures) to resolve the issue

### Supported/unsupported scenarios

* Is your workload **on supported configuration to perform Disaster Recovery or migration**? Ensure that the workload falls under our [support matrix](https://docs.microsoft.com/azure/site-recovery/vmware-physical-azure-support-matrix).
* **Windows Server 2019 Operating System** can be protected by Azure Site Recovery **version 9.22**. Follow guidelines given [here](https://docs.microsoft.com/azure/site-recovery/service-updates-how-to#between-an-on-premises-vmware-or-physical-site-to-azure) to upgrade your Site Recovery components.
* [If OS disk is a dynamic disk, it is not supported. **Data disk can be  a dynamic disk**](https://docs.microsoft.com/azure/site-recovery/vmware-physical-azure-support-matrix#storage)
* [**Unsupported operating systems**](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#unsupported-operating-systems)

**Unsupported Boot configurations**

* [Boot disk not found (Error 95310)](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#boot-and-system-partitions--volumes-are-not-the-same-disk-errorid-95309)
* [Multiple Boot disks found (Error 95311)](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#boot-and-system-partitions--volumes-are-not-the-same-disk-errorid-95309)
* [System and boot partitions/volumes on different disks **(Error 95309)**](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#boot-and-system-partitions--volumes-are-not-the-same-disk-errorid-95309)

**Supported disk size**

* Data disk must be between 1024 **MB** and 4095 **GB**
* Operating system disk size must be between 1024 **MB** and 2048 **GB**. Learn [more](https://docs.microsoft.com/azure/site-recovery/vmware-physical-azure-support-matrix#azure-vm-requirements).

### Troubleshoot mobility agent installation failures

* **[Prerequisites]** To quickly unblock mobility agent installation failures, ensure push installation prerequisites for [Windows](https://docs.microsoft.com/azure/site-recovery/vmware-azure-install-mobility-service#prepare-for-a-push-installation-on-a-windows-computer) and [Linux](https://docs.microsoft.com/azure/site-recovery/vmware-azure-install-mobility-service#prepare-for-a-push-installation-on-a-linux-server) are met.
* [**Credential/privilege errors** (Error ID: 95107, 95108, 95517, 95518)](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#credentials-check-errorid-95107--95108)
* [**Login failures** (Error ID: 95519, 95520, 95521, 95522)](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#credentials-check-errorid-95107--95108)
* [**Connectivity errors** (Error ID: 95117, 95118)](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#connectivity-failure-errorid-95117--97118)
* [**File sharing, printer/WMI configuration errors** (Error ID: 95105, 95106, 95103)](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#file-and-printer-sharing-services-check-errorid-95105--95106)
* [**VSS installation failures**](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#vss-installation-failures)

### Upgrade

* Looking for **latest release notes**? Access all Site Recovery release notes [here](https://docs.microsoft.com/azure/site-recovery/service-updates-how-to#links-to-currently-supported-update-rollups).
* **Unable to upgrade mobility agent**? Ensure the [support statement requirements and upgrade guidelines](https://docs.microsoft.com/azure/site-recovery/service-updates-how-to) are met.

### Troubleshoot replication errors

* Replication issues due to **high churn**? Read the [capacity planning document](https://docs.microsoft.com/azure/site-recovery/site-recovery-plan-capacity-vmware#capacity-considerations) to verify your configurations.
* Troubleshoot [initial replication issues](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-replication).
* [Upgrade to the latest version to fix known issues](https://docs.microsoft.com/azure/site-recovery/service-updates-how-to#between-an-on-premises-vmware-or-physical-site-to-azure)

### Pricing

* Frequently asked questions on **Licensing policy, Azure Hybrid benefit, charges incurred during migration and Disaster Recovery** can be found [here](https://azure.microsoft.com/pricing/details/site-recovery/)
* Want to **estimate your costs for Site recovery usage**? Use our [pricing calculator](https://azure.microsoft.com/pricing/calculator/?service=site-recovery). For detailed estimates, run our [deployment planner tool](https://docs.microsoft.com/azure/site-recovery/site-recovery-deployment-planner).
