<properties
  pagetitle="Failback failed"
  description="Questions or issues related to failback operation failures"
  service="microsoft.recoveryservices"
  resource="vaults"
  ms.author="sideeksh,sharrai"
  selfhelptype="Generic"
  supporttopicids="32786264"
  resourcetags=""
  productpesids="16370"
  cloudenvironments="blackforest,fairfax,public,usnat,ussec,mooncake"
  disableclouds=""
  articleid="dd1ed9ea-b3b7-4440-97bb-7b0f3febd0a9"
  ownershipid="Compute_SiteRecovery" />
# Failback failed

## **Recommended Steps**

* [Migrate AWS VMs to Azure](https://go.microsoft.com/fwlink/?linkid=2137866)
* [Migrate physical servers/bare metal servers to Azure](https://go.microsoft.com/fwlink/?linkid=2137867)
* [Migrate servers from other clouds (GCP, IBM Cloud, etc.) to Azure](https://go.microsoft.com/fwlink/?linkid=2137963). You can migrate most x64 servers by treating them as physical servers for the purpose of migration.
* [Migrate Azure VMs from one Azure region to another using Azure Site Recovery (ASR)](https://go.microsoft.com/fwlink/?linkid=2137868)

### **Replication of VMware virtual machines**

**Replication is stuck at 0%**

If there are multiple VMs that are replicating, initial replication for the VMs will be sequenced in batches. Initial replication may seem to be stuck at 0% for VMs that are sequenced behind others.  Check replication events for the VM to see if there are any errors. If there are no errors, wait for initial replication for the other VMs to complete.

**Bandwidth throttling for replication**

* You can control the bandwidth used by the Azure Migrate appliance for replication using [Windows NetQosPolicy](https://go.microsoft.com/fwlink/?linkid=2137869)

**Replication cycle failed with error "No disk snapshots were found for snapshot replication"**

This error occurs when a storage vMotion happens on a virtual machine under replication. Storage vMotion of a virtual machine under replication is currently not supported.

- Storage vMotion the virtual machine back to its original datastore to allow subsequent replication cycles to proceed
- Else, stop replication for the virtual machine and configure replication again. This is equivalent to a fresh replication of the virtual machine after the storage vMotion.

**Troubleshoot connectivity between the Mobility service on the replicating machine and the Configuration Server, and between the replicating machine and a Scale-out Process Server**

- Ensure that the Mobility Service software on the replicating machine is in a running state running. On Windows machines open services (Run > services.msc) and validate that the "InMage Scout VX Agent – Sentinel/Outpost" is running. On Linux, run `sudo ps -ef | grep Vx` and ensure that the Vx agent process is running.
- Validate that the Mobility service on the replicating machine is able to connect to the Configuration Server on TCP ports 443 and 9443, and if you are using a scale-out process server that it is able to connect to the Process Server on TCP port 9443

  - **Checking connectivity to Configuration Server from a Windows machine:** Log in to the machine and open PowerShell. In PowerShell run `Test-NetConnection <ConfigurationServer IP address> - Port 443` and `Test-NetConnection <ConfigurationServer IP address> -Port 9443`. The cmdlet should return `TcpTestSucceeded : True` if connectivity exists.
  - **Checking connectivity to Scale-out Process Server from a Windows machine:** Log in to the machine and open PowerShell. In PowerShell run `Test-NetConnection <Scale-OutProcessServer IP address> -Port 9443`. The cmdlet should return `TcpTestSucceeded : True` if connectivity exists.
  - **Checking connectivity to Configuration Server from a Linux machine:** Log in to the Linux machine and open shell. Use the telnet utility to test connectivity to TCP ports 443 and 9443 of the Configuration Server. Run `telnet <ConfigurationServerIPAddress>:443` and `telnet <ConfigurationServerIPAddress>:9443`. If connectivity exists the telnet client will be able to open these connections to the Configuration Server.
  - **Checking connectivity to scale-out Process Server from a Linux machine:** Log in to the Linux machine and open shell. Run `telnet <Scale-OutProcessServerIPAddress>:9443`. If connectivity exists the telnet client will be able to open a connection on port 9443 of the scale-out Process Server.
Connectivity from the Mobility service to the Configuration Server or Process Server could be impacted due to one of these reasons:

* The network communication paths have been blocked off due to a firewall or routing configuration
* The Configuration Server or Process Server machines are powered off
* The Configuration Server process ('cxpsprocessserver' in services.msc) that listens on port 443 is not running
* The Process Server process ('tmansvc' in services.msc) than listens on port 9443 is not running

**Installation issues with Mobility service agent**

1. Machines with Secure Boot aren't supported. Disable Secure Boot, and retry installation. 
2. Check if installation failed due to missing [OS updates](https://go.microsoft.com/fwlink/?linkid=2137871)
3. Check if installation failed due to insufficient boot space on [Linux VMs](https://go.microsoft.com/fwlink/?linkid=2137964)

**Error 78188: Replication critical due to high churn**

This can happen when the data change rate (write bytes/sec) on the disks of the virtual machines under replication is more than the [supported limits](https://go.microsoft.com/fwlink/?linkid=2137870) for the target disks.

If you see this issue consistently, use Premium Managed Disks. If you're replicating to Standard HDD/SSD, then upgrade to Premium SSD. To do this, disable replication for the VM, and enable replication again with Premium SSD disks selected for replication.