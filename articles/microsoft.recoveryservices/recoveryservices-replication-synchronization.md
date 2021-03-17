<properties
  pagetitle="Initial replication/synchronization is not progressing"
  description="Questions or issues related to initial replication being stuck or taking longer than expected"
  service="microsoft.recoveryservices"
  resource="vaults"
  ms.author="sideeksh,sharrai"
  selfhelptype="Generic"
  supporttopicids="32745021"
  resourcetags=""
  productpesids="16370"
  cloudenvironments="fairfax,mooncake,public,usnat,ussec,blackforest"
  disableclouds=""
  articleid="e57ec17f-4ba7-47e4-8b01-79e1d9773e41"
  ownershipid="Compute_SiteRecovery" />
# Initial replication/synchronization is not progressing

## **Recommended Steps**

Before you start, review the following documents according to appropriate scenario:
- [Azure to Azure disaster recovery architecture](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-architecture).
- [VMware to Azure disaster recovery architecture](https://docs.microsoft.com/azure/site-recovery/vmware-azure-architecture).
- [Hyper-V to Azure disaster recovery architecture](https://docs.microsoft.com/azure/site-recovery/hyper-v-azure-architecture).

### **Common issues and solutions**

- Initial replication is stuck at 0%.
    - If multiple VMs are replicating, then initial replication for the VMs will be sequenced in batches. Initial replication for VMs that are sequenced behind others may appear to be stuck at 0%. Make sure to check replication events for the VM to see if there are any errors. 
    - If the outbound access for your source machines is controlled with URLs, then ensure that you have allowed the access to required URLs for communication with Azure Site Recovery services. Refer to these required URLs depending on if:
        - [Source machine is an Azure VM](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-architecture#outbound-connectivity-urls)
        - [Source machine is a Hyper-V VM](https://docs.microsoft.com/azure/site-recovery/hyper-v-azure-architecture#outbound-connectivity-for-urls)
        - [Source machine is a VMware/Physical VM](https://docs.microsoft.com/azure/site-recovery/vmware-azure-architecture#outbound-connectivity-for-urls)
    - For VMware/Physical machines, check if there is connectivity between the Configuration server and Azure. Port 9443 is the default port used for sending and receiving replication traffic, but you can modify this port number. In addition to the port 9443, we also open port 443. Ensure these ports on the Configuration server and process server are not blocked or being used by another service.
    
    - If antivirus software has been installed on your VMware/Physical environment, exclude [these](https://docs.microsoft.com/azure/site-recovery/vmware-azure-set-up-source#azure-site-recovery-folder-exclusions-from-antivirus-program) folders for smooth replication.
    - For Hyper-V machines, ensure that the correct MARS agent version has been installed. Installing the MARS agent for Azure Backup or using an incorrect version might cause this issue. Check the latest MARS version [here](https://docs.microsoft.com/azure/site-recovery/site-recovery-whats-new).

- Unable to enable replication.
    - If you’re using a custom DNS for your Azure machines, make sure that the DNS server is accessible from the disaster recovery region by following the steps [here](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-troubleshoot-errors?#outbound-urls-or-ip-ranges-error-code-151037-or-151072).
    - For you Azure machines, ensure that you have the latest TLS certificates enabled. To do so you can either allow list the URLs mentioned [here](https://docs.microsoft.com/azure/security/fundamentals/tls-certificate-changes) or update them manually by following the steps mentioned [here](https://techcommunity.microsoft.com/t5/azure-storage/azure-storage-tls-changes-are-coming-and-why-you-care/ba-p/1705518).
    
    - For VMware machines, ensure that the [File and Printer sharing service is enabled](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#file-and-printer-sharing-services-check-errorid-95105--95106) and [WMI service is enabled](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#windows-management-instrumentation-wmi-configuration-check-error-code-95103) on your virtual machine. Also ensure that the [network shared folders on your virtual machine are accessible](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#check-access-for-network-shared-folders-on-source-machine-errorid-9510595523) from the process server.

- Data uploading slowly.
    - If your data is uploading slowly then make sure to check Azure Site Recovery [data churn limits](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-troubleshoot-replication#azure-site-recovery-limits). If the churn is high, then try to switch to a premium disk or reduce the churn.
