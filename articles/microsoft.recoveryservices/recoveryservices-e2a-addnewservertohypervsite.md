<properties
  pagetitle="Site Recovery (VMM to Azure)/Site Recovery provider setup and registration&#xD;"
  description="Site Recovery (VMM to Azure)/Site Recovery provider setup and registration"
  service="microsoft.recoveryservices"
  resource="vaults"
  ms.author="sharrai"
  selfhelptype="Generic"
  supporttopicids="32786261"
  resourcetags=""
  productpesids="16370"
  cloudenvironments="blackforest,fairfax,public,usnat,ussec,mooncake"
  disableclouds=""
  articleid="149aa758-e4a5-473b-8a18-4a4376439aa0"
  ownershipid="Compute_SiteRecovery" />
# Site Recovery (VMM to Azure)/Site Recovery provider setup and registration

## **Recommended Steps**

### **Errors while installing the Hyper-V replication provider**

The Hyper-V replication provider (AzureSiteRecoveryProvider.exe) should be installed on the Hyper-V host servers that hosts the virtual machines to be migrated. The Hyper-V hosts server must be on Windows Server 2012 R2 or a later version of Windows Server, and should have .NET framework 4.0/.30319 or later.

For Hyper-V hosts that are on a version of Hyper-V older than Windows Server 2012 R2, consider using the [agent-based replication of physical and non-virtualized servers](https://docs.microsoft.com/azure/migrate/tutorial-migrate-physical-virtual-machines)] method instead to migrate the Hyper-V virtual machines.

### **I get an error that says that the Hyper-V host is already registered to a Recovery Services vault.**

The registration step connects the replication provider software installed on Hyper-V host to the Azure Migrate: Server Migration. The replication provider component is also used by Azure Site Recovery to provide disaster recovery for Hyper-V virtual machines. If you see a message indicating that the Hyper-V host is already registered to a Recovery Services vault, this most likely is because the Hyper-V host is configured for disaster recovery with Azure Site Recovery, or because the Hyper-V host is already registered to a different Azure Migrate: Server Migration project.

Registering the Hyper-V host with two instances of Azure Migrate: Server Migration is not supported.<br>
If the Hyper-V host is already being using with Azure Site Recovery, consider using the [agent-based replication of physical and non-virtualized servers](https://docs.microsoft.com/azure/migrate/tutorial-migrate-physical-virtual-machines)] method instead to migrate the Hyper-V virtual machines.

### **I get an error while finalizing registration for the Hyper-V host**

After the replication provider is installed on the Hyper-V host and the registration has been completed using the registration key, you'll need to finalize the registration from the portal experience for the Server Migration tool. If the finalize registration step fails, retry the operation again as the error may be a transient. If the finalize registration operation continues to fail, you can troubleshoot further by going to the Server Migration jobs page. 

To see failed jobs:<br>
1. Go to the Servers page of the Azure Migrate portal experience and select **Overview** on the Server Migration tile. 
2. In the Server Migration overview page that opens select '**Jobs** from the left menu to see a list of jobs. 
3. Right-click the failed job and select the error details to troubleshoot further.

### **Where can I find the URLs that need access for Hyper-V migration in Azure Government**

The replication provider software on the Hyper-V hosts will need access to the URLs mentioned [here](https://docs.microsoft.com/azure/migrate/migrate-support-matrix-hyper-v-migration#url-access-azure-government).
