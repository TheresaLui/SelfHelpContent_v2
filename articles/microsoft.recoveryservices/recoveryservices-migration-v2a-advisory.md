<properties
    pageTitle="Site Recovery (VMware to Azure) Advisory"
    description="Site Recovery (VMware to Azure) Advisory"
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="asgang,TobyTu"
    ms.author="asgang"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32680612"
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="75642b51-f522-4acb-9ef4-f78c5e87ec25"
	ownershipId="Compute_SiteRecovery"
/>

# Advisory questions - VMware/Physical to Azure

## **Recommended Documents**

### Getting started with Site Recovery

* **Planning**: Trying to identify Site Recovery resources required to protect your workload? Run our [deployment planner tool](https://docs.microsoft.com/azure/site-recovery/site-recovery-deployment-planner) to obtain **customized guidance on requirements, cost estimates** & supported configurations
* [Azure Site Recovery FAQ](https://docs.microsoft.com/azure/site-recovery/vmware-azure-common-questions)
* Start replicating [**VMware VMs to Azure**]( https://docs.microsoft.com/azure/site-recovery/vmware-azure-set-up-source) with ASR
* Start replicating [**Physical machines to Azure**]( https://docs.microsoft.com/azure/site-recovery/physical-azure-set-up-source) with ASR
* **Overview**: Refer to [Azure Site Recovery architecture](https://docs.microsoft.com/azure/site-recovery/vmware-azure-architecture) & [VMware to Azure overview](https://docs.microsoft.com/azure/site-recovery/vmware-azure-about-disaster-recovery) for details on Site Recovery

### Pricing

* Frequently asked questions on **Licensing policy, Azure Hybrid benefit, charges incurred during migration and Disaster Recovery** can be found [here](https://azure.microsoft.com/pricing/details/site-recovery/)
* Want to **estimate your costs for Site recovery usage**? Use our [pricing calculator](https://azure.microsoft.com/pricing/calculator/). For detailed estimates, run our [deployment planner tool](https://docs.microsoft.com/azure/site-recovery/site-recovery-deployment-planner)

### Supported/unsupported configuration

* Is your workload **supported for Disaster Recovery or for migration**? Ensure that the workload falls under our [support matrix](https://docs.microsoft.com/azure/site-recovery/vmware-physical-azure-support-matrix)

### Networking

* Learn about [**how to retain IP address** for Azure VMs after failover](https://docs.microsoft.com/azure/site-recovery/concepts-on-premises-to-azure-networking#retaining-ip-addresses)
* Learn about [Network Security Groups(NSG)](https://docs.microsoft.com/azure/site-recovery/concepts-network-security-group-with-site-recovery), [traffic manager](https://docs.microsoft.com/azure/site-recovery/concepts-traffic-manager-with-site-recovery) & [Express Route](https://docs.microsoft.com/azure/site-recovery/concepts-expressroute-with-site-recovery) with Azure Site Recovery
* Learn about [Network Security Groups(NSG)](https://docs.microsoft.com/azure/site-recovery/concepts-network-security-group-with-site-recovery), [traffic manager](https://docs.microsoft.com/azure/site-recovery/concepts-traffic-manager-with-site-recovery) & [Express Route](https://docs.microsoft.com/azure/site-recovery/concepts-expressroute-with-site-recovery) with Azure Site Recovery

### Replication

* Want to protect **application workloads (say Active Directory, SQL server etc.,)** through site recovery? For more information, see [What workloads can you protect with Azure Site Recovery?](https://docs.microsoft.com/azure/site-recovery/site-recovery-workload)
* **Anti-virus**: [Manage Site Recovery folders](https://docs.microsoft.com/azure/site-recovery/vmware-azure-set-up-source#azure-site-recovery-folder-exclusions-from-antivirus-program) from your anti-virus software to ensure smooth replication
* Virtual machine **unavailable on Azure portal to enable protection**? Click [here](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-replication#step-3-troubleshoot-source-machines-that-arent-available-for-replication) to resolve

### Site Recovery Infrastructure

* Install new instance of [Configuration Server using OVF template](https://docs.microsoft.com/azure/site-recovery/tutorial-vmware-to-azure#download-the-vm-template)
* [Techniques to deploy new instance of Mobility service](https://docs.microsoft.com/azure/site-recovery/vmware-azure-install-mobility-service)
* **Upgrade**: To upgrade Configuration server, Process Server, Mobility agent to **latest versions**, refer to [our support statement & upgrade guidance](https://docs.microsoft.com/azure/site-recovery/service-updates-how-to)
* **Manage**: Want to manage your Site recovery components, click [here](https://docs.microsoft.com/azure/site-recovery/vmware-azure-manage-configuration-server)

### Troubleshoot

* [Troubleshoot mobility agent installation errors](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install)
* [Troubleshoot configuration server errors](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-configuration-server)
* [Troubleshoot replication errors](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-replication)
* [Troubleshoot failover/failback errors](https://docs.microsoft.com/azure/site-recovery/site-recovery-failover-to-azure-troubleshoot)

### Migration

* Want to migrate your workload to Azure? Learn [more](https://docs.microsoft.com/azure/site-recovery/migrate-overview)
