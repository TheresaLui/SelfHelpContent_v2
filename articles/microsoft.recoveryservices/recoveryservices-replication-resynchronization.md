<properties
  pagetitle="I need help with resynchronization"
  description="Questions or issues related to resync failures"
  service="microsoft.recoveryservices"
  resource="vaults"
  ms.author="sharrai"
  selfhelptype="Generic"
  supporttopicids="32745015"
  resourcetags=""
  productpesids="16370"
  cloudenvironments="blackforest,fairfax,public,usnat,ussec,mooncake"
  disableclouds=""
  articleid="37f9bdea-af30-4a87-98d6-e02e95b90364"
  ownershipid="Compute_SiteRecovery" />
# I need help with resynchronization

## **Recommended Documents**

### Common issues and solutions

- Why is resynchronization required for my machine.
    - Adding a new disk or removing an existing disk can cause the "resynchronization required" alert to be triggered. 
        - If a replicating disk was removed, add it back to the machine. 
        - If the disk signature for a replicating disk was changed, revert the signature back to the older one. 
        - If a replicating disk was unattached, attached to the VM again.
        - If any of the above is not possible, disable and re-enable protection for the machine. Follow these steps: Navigate to Azure Portal > Go to the Recovery Services Vault > Open Replicated Items > Click on the concerned machine's overview > Click Disable replication. Once it is disabled, you can enable replication again.
    - Resynchronization is required for Hyper-V machine due to large amount of HRL files accumulated on the source machine. 
        - If the amount of HRL files is growing on your source machine, then it could be caused due to insufficient network bandwidth. This will cause the backlog to grow and ultimately result in a resynchronization required alert. 
        - To resolve the issue, trigger resynchronization. Follow these steps: Navigate to Azure Portal > Go to the Recovery Services Vault > Open Replicated Items > Click on the concerned machine's overview > Click Resynchronize.

- Replication is not progressing for the source machine.
    - Ensure that you have checked the supported [data churn limits](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-troubleshoot-replication#azure-site-recovery-limits) of Azure Site Recovery. A higher data churn will cause the replication to slow down. If the churn is high, then try to switch to a premium disk or reduce the churn. 
    - For VMware/Physical machines, ensure that the configuration server and process server are in a healthy state and [all the services required for replication](https://docs.microsoft.com/azure/site-recovery/vmware-physical-azure-troubleshoot-process-server#step-2-check-process-server-services) are running. Also, make sure that the system time is in sync with the global time.
    - Ensure that there is connectivity between configuration server and source machine. To do so, check the [network requirements](https://docs.microsoft.com/azure/site-recovery/vmware-azure-deploy-configuration-server#network-requirements).
    - If your infrastructure is using an NVA appliance or has proxy enabled then make sure that the required URLs have been whitelisted for connection with Azure Site Recovery services. Refer to these required URLs depending on if:
        - [Source machine is an Azure VM](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-architecture#outbound-connectivity-urls).
        - [Source machine is a Hyper-V VM](https://docs.microsoft.com/azure/site-recovery/hyper-v-azure-architecture#outbound-connectivity-for-urls).
        - [Source machine is a VMware/Physical machine](https://docs.microsoft.com/azure/site-recovery/vmware-azure-architecture#outbound-connectivity-for-urls). 
    - Secure Boot UEFI has been enabled on your source machine. Azure machines do not support secure boot, so make sure it has been disabled on your source machine too.
    - If your replication is not progressing after agent upgrade on Hyper-V hosts, ensure that the correct MARS agent and Microsoft Azure Site Recovery Provider versions have been installed. Installing the MARS agent for Azure Backup or installing mismatching versions of MARS and Microsoft Azure Site Recovery Provider might cause this issue. Check the latest MARS and Microsoft Azure Site Recovery Provider version [here](https://docs.microsoft.com/azure/site-recovery/site-recovery-whats-new).

- Need help with moving configuration server to a new vault
    - If you plan to move your configuration server to a different vault then follow [these](https://docs.microsoft.com/azure/site-recovery/vmware-azure-manage-configuration-server#register-a-configuration-server-with-a-different-vault) steps. Note that moving the configuration server will stop the replication of all protected virtual machines under it and replication will have to be enabled again.

- Proximity Placement Groups for unmanaged disks (storage accounts) are not supported. To use proximity placement groups, ensure that you have used managed disks to setup replication. To setup replication to proximity placement groups, check the steps mentioned [here](https://docs.microsoft.com/azure/site-recovery/how-to-enable-replication-proximity-placement-groups#set-up-disaster-recovery-for-vms-in-proximity-placement-groups-via-portal).