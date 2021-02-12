<properties
    pageTitle="Stop replication"
    description="Troubleshoot errors in the stop replication operation"
    service="microsoft.migrate"
    resource="migrateprojects"
    authors="bsiva"
    ms.author="bsiva"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32675758"
    resourceTags=""
    productPesIds="16348"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="1d5b47af-5ee0-49a6-af97-46e2d6544523"
	ownershipId="Compute_AzureMigrate"
/>

# Stop replication/Disable replication for a virtual machine

## **Recommended Steps**

## Agentless replication of VMWare virtual machines

### *I get an error that says 'could not complete the job in the allotted time'*

This error happens if either:

- A snapshot consolidation (merge snapshot) operation is in progress for the virtual machine at the time the 'Stop replication' action is initiated, and the stop replication task timed out waiting for the consolidate operation to complete

- This may also occur if the Azure Migrate appliance is turned off, or if the Azure Migrate appliance (specifically the 'Azure Migrate Replication Gateway' service on the appliance) is unable to communicate with the Server Migration tool

In both these cases, the failure is likely to be a transient issue.

- If a consolidate operation is in progress for the virtual machine, wait for the operation to complete before retrying. You can monitor the currently active tasks on the virtual machine from the tasks view in vCenter. 

- If the appliance is turned off, turn on the appliance and then retry. If the 'Azure Migrate Replication Gateway service' (from services.msc on the appliance) is not running, restart the 'Azure Migrate Replication Gateway service' on the appliance and then retry. 

- If the appliance has been deleted or is no longer available on-premises retry again after some time (15-20 minutes)

## Agent based replication of VMware virtual machines and Physical servers

### **I get an error that says the on-premises server isn't connected**

This happens when the on-premises vCenter Server/physical server, or the Replication appliance (Configuration Server) isn't connected to Server Migration tool. To check connectivity status of the replication appliance/vCenter Server/physical server, click 'Overview' on the Server Migration tile, then click 'Infrastructure Servers' on the left menu. The infrastructure servers page shows the list of registered replication appliances and Hyper-V host server's and their connection status.

If the replication appliance/vCenter Server/physical server isn't connected, ensure that they are running, have internet connectivity. Open Services MMC (Run >services.msc), and ensure the 'Microsoft Azure Site Recovery Service' service is running. Retry the operation after fixing the connectivity issues between the replication appliance/vCenter Server/physical server and the Server Migration tool.
If the replication appliance/vCenter Server/physical server is no longer available, then select the 'Force Remove' option while stopping replication for the machine.

## Agentless replication of Hyper-V virtual machines.

### **I get an error that says the on-premises server isn't connected**

This happens when the on-premises Hyper-V host isn't connected to Server Migration tool. To check connectivity status of the Hyper-V hosts, click 'Overview' on the Server Migration tile, then click 'Infrastructure Servers' on the left menu. The infrastructure servers page shows the list of registered  Hyper-V host server's and their connection status.

If the Hyper-V servers aren't connected, ensure that they are running, and have internet connectivity. Open Services MMC (Run >services.msc), and ensure the 'Microsoft Azure Site Recovery Service' service is running. Retry the operation after fixing the connectivity issues between the Hyper-V host server and the Server Migration tool.

If the Hyper-V hosts are no longer available, then select the 'Force Remove' option while stopping replication for the machine.
