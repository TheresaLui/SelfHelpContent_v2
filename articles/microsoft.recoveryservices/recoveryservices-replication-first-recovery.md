<properties
  pagetitle="The first recovery point did not get generated"
  description="Questions or issues related to the first recovery point not being generated"
  service="microsoft.recoveryservices"
  resource="vaults"
  ms.author="sideeksh,sharrai"
  selfhelptype="Generic"
  supporttopicids="32745027"
  resourcetags=""
  productpesids="16370"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="8705922f-8944-4505-82bd-c559b591b6ee"
  ownershipid="Compute_SiteRecovery" />
# The first recovery point did not get generated


Refer to the following steps to resolve issues with the first recovery point not being generated.

## **Recommended Steps**

**Mobility service installation is failing**
- Ensure that sufficient free space available on your disks. It is recommended to have at least 1 GB free space on your disks for successful installation of mobility service.
- For VMware machines, you can go ahead and install the mobility service manually too. Check the steps [here](https://docs.microsoft.com/azure/site-recovery/vmware-azure-install-mobility-service).

**High data churn on your source machines**
<br>This is most common reason for a recovery point not getting generated. 
- Ensure that you have checked the supported [data churn limits](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-troubleshoot-replication#azure-site-recovery-limits) of Azure Site Recovery.

**Constricted network bandwidth**
<br>Network bandwidth may end up constricting your data transfer and causing the recovery point generation to fail. 
- Ensure that adequate network bandwidth is available for replication to progress.

**Machine has been migrated from VMware to Azure**
<br>If your machine has been migrated from VMware to Azure and the first recovery point is not getting generated on your machine, then follow these steps.
1. Check the current installation path by running the following command: 
   ` cat /usr/local/.vx_version | grep INSTALLATION_DIR`
      
2. Stop services by running the following command: 

    `/usr/local/ASR/Vx/bin/stop`
  
3. Edit the file `/usr/local/ASR/Vx/etc/drscout.conf` to modify the following entry: 
   <br>from `DiffSourceExePathname=/usr/local/ASR/Vx/bin/s2V2A` 
   <br>to `DiffSourceExePathname=/usr/local/ASR/Vx/bin/s2A2A`
  
4. Start services by running the following command: 
 
    `/usr/local/ASR/Vx/bin/start`
