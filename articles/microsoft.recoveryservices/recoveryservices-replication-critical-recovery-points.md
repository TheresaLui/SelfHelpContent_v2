<properties
  pagetitle="Critical events are generated even though latest recovery points are available&#xD;"
  description="Questions or issues related to critical events generated despite availability of latest recovery points"
  service="microsoft.recoveryservices"
  resource="vaults"
  ms.author="sideeksh"
  selfhelptype="Generic"
  supporttopicids="32744977"
  resourcetags=""
  productpesids="16370"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="b909eeb0-c468-41cf-8c14-fc8a83ab1796"
  ownershipid="Compute_SiteRecovery" />
# Critical events are generated even though latest recovery points are available

## **Recommended Documents**

- High churn on disks can often result in recovery point unavailability and/or critical event generation. [Ensure that data change rates/churn are within the limits](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-troubleshoot-replication#high-data-change-rate-on-the-source-virtal-machine).
- If you're looking to upgrade your Site Recovery agent to the latest version, refer to [updates and component upgrades in Azure Site Recovery](https://docs.microsoft.com/azure/site-recovery/service-updates-how-to).
- If you're running into issues related to replication for VMs encrypted using Azure Disk Encryption, review [Enable replication for encrypted Azure VMs in Azure Site Recovery](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-how-to-enable-replication-ade-vms)
- If you suspect that a networking related issue is causing the generation of critical alerts, review our [Networking guidance for replicating Azure virtual machines](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-about-networking). Among other concepts, the document also outlines what you need to do to ensure outbound connectivity of your VM.
- If you're planning for bandwidth requirements for Site Recovery when setting up replication for on prem servers or virtual machines, please review our document on [plan capacity for VMware disaster recovery with Azure Site Recovery](https://docs.microsoft.com/azure/site-recovery/site-recovery-plan-capacity-vmware)
- Is your cache storage account maxed out? Are you unable to upload replication logs to cache storage account? Please review our guidance on how many VMs you can replicate per cache storage account in the [support matrix for VMware/physical disaster recovery in Azure Site Recovery](https://docs.microsoft.com/azure/site-recovery/vmware-physical-azure-support-matrix) and [support matrix for Azure VM disaster recovery with Azure Site Recovery](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-support-matrix)
- If app consistent recovery points aren't being generated, [ensure that Site Recovery VSS provider is installed on the machine](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install). If not, complete installation. If it's correctly installed, [ensure that Site Recovery VSS provider is running on the machine](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-replication). If not, start the services.
- If you're running SQL on your VMs and recovery points are not being generated on them, check if you have encountered the following known issues: 
    - [Known issue is SQL Server instances with AUTO_CLOSE DBs](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-troubleshoot-replication)
    - [Known issue in SQL Server 2008 R2](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-troubleshoot-replication)
