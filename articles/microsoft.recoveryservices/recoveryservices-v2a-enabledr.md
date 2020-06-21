<properties
	pageTitle="Site Recovery (VMware to Azure)/Enable Protection"
	description="Site Recovery (VMware to Azure)/Common issues during Enable Protection"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="asgang"
	ms.author="asgang"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32536405"
	resourceTags=""
	productPesIds="16370"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="76736774-887b-41c7-97ab-4463cd31a739"
	ownershipId="Compute_SiteRecovery"
/>

# Enable Protection - VMware/Physical to Azure

## **Recommended Documents**

### Getting started

* **[Planning]** Trying to identify Site Recovery resources required to protect your workload? Run our [deployment planner tool](https://aka.ms/siterecovery_deployment_planner) to obtain customized guidance on requirements, cost estimates & supported configurations.
* **Not able to find/select virtual machine on Azure portal** during Enable Replication? Click [here](https://aka.ms/doc-plugin-VM-not-showing) to resolve.
* Refer to the FAQ on Azure Site Recovery [here](https://aka.ms/asr_v2a_faq)
* Want to protect **application workloads (say Active Directory, SQL server etc.,)** through site recovery? **Learn [more](https://aka.ms/asr_workload)** 
* **[Anti-virus]** [Manage Site Recovery folders](https://aka.ms/asr_antivirus_exclusion) from your anti-virus software to ensure smooth replication

### Networking/connectivity

* Ensure that all URLs mentioned [here](https://aka.ms/asr_CS_prereq) are allowed on configuration server directly or via proxy for successful replication
* vCenter connectivity/discovery failure? Follow the guidelines given [here](https://aka.ms/asr_v2a_vcenter_discovery_troubleshoot) to resolve the issue

### Supported/unsupported scenarios

* Is your workload **on supported configuration to perform Disaster Recovery or migration**? Ensure that the workload falls under our [support matrix](https://aka.ms/asr_v2a_support_matrix).
* **Windows Server 2019 Operating System** can be protected by Azure Site Recovery **version 9.22**. Follow guidelines given [here](https://aka.ms/asr_vmware_upgrades) to upgrade your Site Recovery components.
* [If OS disk is a dynamic disk, it is not supported. **Data disk can be  a dynamic disk**](https://docs.microsoft.com/azure/site-recovery/vmware-physical-azure-support-matrix#storage)
* [**Unsupported operating systems**](https://aka.ms/ASR_unsupported_OS)

#### Unsupported Boot configurations

* [Boot disk not found (Error 95310)](https://aka.ms/asr_boot_failures)
* [Multiple Boot disks found (Error 95311)](https://aka.ms/asr_boot_failures)
* [System and boot partitions/volumes on different disks **(Error 95309)**](https://aka.ms/asr_boot_failures)

#### Supported disk size

* Data disk must be between 1024 **MB** and 4095 **GB**
* Operating system disk size must be between 1024 **MB** and 2048 **GB**. Learn [more](https://docs.microsoft.com/azure/site-recovery/vmware-physical-azure-support-matrix#azure-vm-requirements).

### Troubleshoot mobility agent installation failures

* **[Prerequisites]** To quickly unblock mobility agent installation failures, ensure push installation prerequisites for [Windows](https://docs.microsoft.com/azure/site-recovery/vmware-azure-install-mobility-service#prepare-for-a-push-installation-on-a-windows-computer) and [Linux](https://docs.microsoft.com/azure/site-recovery/vmware-azure-install-mobility-service#prepare-for-a-push-installation-on-a-linux-server) are met.
* [**Credential/privilege errors** (Error ID: 95107, 95108, 95517, 95518)](https://aka.ms/installation_credential_failures)
* [**Login failures** (Error ID: 95519, 95520, 95521, 95522)](https://aka.ms/installation_login_failures)
* [**Connectivity errors** (Error ID: 95117, 95118)](https://aka.ms/installation_connectivity_failures)
* [**File sharing, printer/WMI configuration errors** (Error ID: 95105, 95106, 95103)](https://aka.ms/installation_File_printer_failures)
* [**VSS installation failures**](https://aka.ms/asr_vss_installation_failures)

### Upgrade

* Looking for **latest release notes**? Access all Site Recovery release notes [here](https://aka.ms/asr_update_rollups).
* **Unable to upgrade mobility agent**? Ensure the [support statement requirements and upgrade guidelines](https://aka.ms/asr_how_to_upgrade) are met.

### Troubleshoot replication errors

* Replication issues due to **high churn**? Read the [capacity planning document](https://docs.microsoft.com/azure/site-recovery/site-recovery-plan-capacity-vmware#capacity-considerations) to verify your configurations.
* Troubleshoot [initial replication issues](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-replication).
* [Upgrade to the latest version to fix known issues](https://aka.ms/asr_vmware_upgrades)

### Pricing

* Frequently asked questions on **Licensing policy, Azure Hybrid benefit, charges incurred during migration and Disaster Recovery** can be found [here](https://aka.ms/asr_pricing)
* Want to **estimate your costs for Site recovery usage**? Use our [pricing calculator](https://aka.ms/asr_pricing_calculator). For detailed estimates, run our [deployment planner tool](https://aka.ms/siterecovery_deployment_planner).
