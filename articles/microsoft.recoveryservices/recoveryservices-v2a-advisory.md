<properties
	pageTitle="Site Recovery (VMware to Azure) Advisory"
	description="Site Recovery (VMware to Azure) Advisory"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="asgang"
	ms.author="asgang"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32630518"
	resourceTags=""
	productPesIds="16370"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="8e138d77-259b-4372-8b67-8531cbb84afc"
	ownershipId="Compute_SiteRecovery"
/>

# Advisory questions - VMware/Physical to Azure

## **Recommended Documents**

### Getting started with Site Recovery

* **[Planning]**: Trying to identify Site Recovery resources required to protect your workload? Run our [deployment planner tool](https://aka.ms/siterecovery_deployment_planner) to obtain **customized guidance on requirements, cost estimates** & supported configurations
* [Azure Site Recovery FAQ](https://docs.microsoft.com/azure/site-recovery/vmware-azure-common-questions)
* Start replicating [**VMware VMs to Azure**]( https://docs.microsoft.com/azure/site-recovery/vmware-azure-set-up-source) with ASR
* Start replicating [**Physical machines to Azure**]( https://docs.microsoft.com/azure/site-recovery/physical-azure-set-up-source) with ASR
* **[Overview]**: Refer to [Azure Site Recovery architecture](https://docs.microsoft.com/azure/site-recovery/vmware-azure-architecture) & [VMware to Azure overview](https://docs.microsoft.com/azure/site-recovery/vmware-azure-about-disaster-recovery) for details on Site Recovery

### Pricing

* Frequently asked questions on **Licensing policy, Azure Hybrid benefit, charges incurred during migration and Disaster Recovery** can be found [here](https://aka.ms/asr_pricing)
* Want to **estimate your costs for Site recovery usage**? Use our [pricing calculator](https://aka.ms/asr_pricing_calculator). For detailed estimates, run our [deployment planner tool](https://aka.ms/siterecovery_deployment_planner).

### Supported/unsupported configuration

* Is your workload **supported for Disaster Recovery or for migration**? Ensure that the workload falls under our [support matrix](https://aka.ms/asr_v2a_support_matrix)

### Networking

* Learn about [**how to retain IP address** for Azure VMs after failover](https://aka.ms/asr_retain_ip)
* Learn about [Network Security Groups(NSG)](https://aka.ms/NSG_ASR), [traffic manager](https://aka.ms/asr_traffic_manager) & [Express Route](https://aka.ms/asr_expressroute) with Azure Site Recovery

### Replication

* Want to protect **application workloads (say Active Directory, SQL server etc.,)** through site recovery? **Learn [more](https://aka.ms/asr_workload)** 
* **[Anti-virus]** [Manage Site Recovery folders](https://aka.ms/asr_antivirus_exclusion) from your anti-virus software to ensure smooth replication.
* Virtual machine **unavailable on Azure portal to enable protection**? Click [here](https://aka.ms/doc-plugin-VM-not-showing) to resolve.

### Site Recovery Infrastructure

* Install new instance of [Configuration Server using OVF template](https://docs.microsoft.com/azure/site-recovery/tutorial-vmware-to-azure#download-the-vm-template)</br>
* [Techniques to deploy new instance of Mobility service](https://docs.microsoft.com/azure/site-recovery/vmware-azure-install-mobility-service)
* **[Upgrade]** To upgrade Configuration server, Process Server, Mobility agent to **latest versions**, refer to [our support statement & upgrade guidance](https://aka.ms/asr_how_to_upgrade).
* **[Manage]** Want to manage your Site recovery components, click [here](https://docs.microsoft.com/azure/site-recovery/vmware-azure-manage-configuration-server)

### Troubleshoot

* [Troubleshoot mobility agent installation errors](https://aka.ms/asr_v2a_push_install)
* [Troubleshoot configuration server errors](https://aka.ms/asr_cs_troubleshoot)
* [Troubleshoot replication errors](https://aka.ms/asr_v2a_replication_troubleshoot)
* [Troubleshoot failover/failback errors](https://aka.ms/asr_v2a_failover_troubleshoot)

### Migration

* Want to migrate your workload to Azure? Learn [more](https://docs.microsoft.com/azure/site-recovery/migrate-overview)
