<properties
	pageTitle="Shared Disk"
	description="Shard Disk on Windows"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="johnnygetHub"
	ms.author="johnnyc"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32740057"
	resourceTags=""
	productPesIds="14749"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="b72d74ed-4885-40ea-abb1-22e750b1a623"
	ownershipId="Compute_VirtualMachines"
/>

# Shared Disk / Virtual Disk Management

4 out of 5 customers resolved their VM virtual disk issue using the below steps.

## **Recommended Steps**

**Azure Shared Disk on Clustered Environments**

Azure Shared Disks provides a consistent experience for applications running on clustered environments today. This means that any application that currently leverages SCSI Persistent Reservations (PR) can use this well-known set of commands to register nodes in the cluster to the disk. The application can then choose from a range of supported access modes for one or more nodes to read or write to the disk. These applications can deploy in highly available configurations while also leveraging Azure Disk durability guarantees.

### Sample workload on Windows

Most Windows-based clustering build on WSFC, which handles all core infrastructure for cluster node communication, allowing your applications to take advantage of parallel access patterns. WSFC enables both CSV and non-CSV-based options depending on your version of Windows Server. For details, refer to [Create a failover cluster](https://docs.microsoft.com/windows-server/failover-clustering/create-failover-cluster).

Some popular applications running on WSFC include:

* SQL Server Failover Cluster Instances (FCI)
* Scale-out File Server (SoFS)
* File Server for General Use (IW workload)
* Remote Desktop Server User Profile Disk (RDS UPD)
* SAP ASCS/SCS

With Azure Shared Disks, customers now have the flexibility to migrate clustered environments running on Windows Server, including Windows Server 2008 (which has reached  [End-of-Support](https://www.microsoft.com/cloud-platform/windows-server-2008)), to Azure. This capability is designed to support [SQL Server Failover Cluster Instances (FCI)](https://docs.microsoft.com/sql/sql-server/failover-clusters/windows/always-on-failover-cluster-instances-sql-server?view=sql-server-ver15#Overview), [Scale-out File Servers (SoFS)](https://docs.microsoft.com/windows-server/failover-clustering/sofs-overview), [Remote Desktop Servers (RDS)](https://docs.microsoft.com/windows-server/remote/remote-desktop-services/rds-plan-high-availability), and [SAP ASCS/SCS](https://docs.microsoft.com/azure/virtual-machines/workloads/sap/) running on Windows Server.

## **Recommended Documents**

* [Azure shared disks](https://docs.microsoft.com/azure/virtual-machines/linux/disks-shared)
* [Enable shared disk](https://docs.microsoft.com/azure/virtual-machines/linux/disks-shared-enable#deploy-an-azure-shared-disk)

**More Information**

* [Overview of Azure Managed Disks](https://docs.microsoft.com/azure/virtual-machines/linux/managed-disks-overview)

**Attaching or Detaching Disks**

* **Attach a new disk** using the [Portal](https://docs.microsoft.com/azure/virtual-machines/linux/attach-disk-portal#attach-a-new-disk) or [CLI](https://docs.microsoft.com/azure/virtual-machines/linux/add-disk#attach-a-new-disk-to-a-vm)<br>
* **Attach an existing disk** using the [Portal](https://docs.microsoft.com/azure/virtual-machines/linux/attach-disk-portal#attach-an-existing-disk) or [CLI](https://docs.microsoft.com/azure/virtual-machines/linux/add-disk#attach-an-existing-disk)<br>
* **Detach a data disk** using the [Portal](https://docs.microsoft.com/azure/virtual-machines/linux/detach-disk#detach-a-data-disk-using-the-portal) or [CLI](https://docs.microsoft.com/azure/virtual-machines/linux/detach-disk#detach-a-data-disk-using-azure-cli)<br>
* [Find and delete unattached Azure managed and unmanaged disks](https://docs.microsoft.com/azure/virtual-machines/linux/find-unattached-disks)
