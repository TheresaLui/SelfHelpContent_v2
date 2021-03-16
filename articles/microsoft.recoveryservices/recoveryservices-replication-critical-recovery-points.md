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

- High churn on disks can often result in recovery point unavailability and/or critical event generation. [Ensure that the data change rates/churn is within the limits](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-troubleshoot-replication#high-data-change-rate-on-the-source-virtal-machine)
- If you are looking to upgrade your Site Recovery agent to the latest version, you can refer our documentation on [updates and component upgrades in Azure Site Recovery](https://docs.microsoft.com/azure/site-recovery/service-updates-how-to)
- If you are running into issues related to replication for VMs encrypted using Azure Disk Encryption, please review our documentation on [enabling replication for encrypted Azure VMs in Azure Site Recovery](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-how-to-enable-replication-ade-vms)
- If you suspect there is a networking related issue causing the generation of critical alerts, please review our note on [networking guidance for replicating Azure virtual machines](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-about-networking). Among other concepts, the document also outlines what you need to do to ensure outbound connectivity of your VM.
- If you are planning for bandwidth requirements for Site Recovery when setting up replication for on prem servers or virtual machines, please review our document on [plan capacity for VMware disaster recovery with Azure Site Recovery](https://docs.microsoft.com/azure/site-recovery/site-recovery-plan-capacity-vmware)
- Is your cache storage account maxed out? Are you unable to upload replication logs to cache storage account? Please review our guidance on how many VMs you can replicate per cache storage account in the [support matrix for VMware/physical disaster recovery in Azure Site Recovery](https://docs.microsoft.com/azure/site-recovery/vmware-physical-azure-support-matrix) and [support matrix for Azure VM disaster recovery with Azure Site Recovery](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-support-matrix)
- If app consistent recovery points are not getting generated, please Ensure that Site Recovery VSS provider is installed on the machine. If not, complete installation. If it is correctly installed, please Ensure that Site Recovery VSS provider is running on the machine. If not, start the services.


- [Steps to configure outbound network connectivity](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-tutorial-enable-replication#configure-outbound-network-connectivity)
- [Review the Support Requirements for all components](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-support-matrix)
- [Steps to enable replication for Azure VMs](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-tutorial-enable-replication)
- [Networking guidance for replicating Azure virtual machines](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-about-networking)
- [Understand the scenario architecture and components](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-architecture)
- [Ensure that Site Recovery VSS provider is installed on the machine. If not, complete installation.](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#vss-installation-failures)
- [Ensure that Site Recovery VSS provider is running on the machine. If not, start the services.](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-replication#missing-app-consistent-recovery-points-error-78144)
- [Known issue is SQL Server instances with AUTO_CLOSE DBs](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-troubleshoot-replication#cause-2-azure-site-recovery-jobs-fail-on-servers-hosting-any-version-of-sql-server-instances-with-auto_close-dbs)
- [Known issue in SQL Server 2008 R2](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-troubleshoot-replication#cause-1-known-issue-on-sql-server-20082008-r2)
- [Ensure that the data change rates/churn is within the limits](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-troubleshoot-replication#high-data-change-rate-on-the-source-virtal-machine)