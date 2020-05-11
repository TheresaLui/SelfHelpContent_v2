<properties
    pageTitle="Azure Migrate: Server Migration replication issues"
    description="Troubleshooting replication issues"
    service="microsoft.migrate"
    resource="migrateprojects"
    authors="bsiva"
    ms.author="bsiva"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32675757"
    resourceTags=""
    productPesIds="16348"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="5a8bcac1-4112-4897-a558-81199f80f5e7"
	ownershipId="Compute_AzureMigrate"
/>

# Azure Migrate: Server Migration replication issues

## **Recommended Steps**

### Agentless replication of VMWare virtual machines

**Receiving transient internal error Azure Migrate**

- Check if appropriate [user access policies](https://docs.microsoft.com/powershell/module/azuread/get-azureaduser?view=azureadps-2.0) are set on the key vault which got created as part of replication
- Switch the user to admin account and set access policies properly
- Retry replication

**When trying to replicate agentless we get "An internal error occurred. Please retry the operation after some time."**

Replace HostName with your ESXi host name where VM belongs in the following steps:

- Is the host name resolvable from the appliance? (Remote desktop into the Azure Migrate appliance, open PowerShell and do an `nslookup` on HostName)
- Is the ping from appliance to the host working? (Remote desktop into to the Azure Migrate appliance, open PowerShell and `ping -4 HostName`)
- Is the port 902 on the host opened? (Remote desktop into the Azure Migrate appliance, open PowerShell and try `Test-NetConnection HostName -port 902` and see if the TCP test succeeds)
- You can add the ESXi host entry into the hosts file of Azure Migrate Appliance, and check if replication starts working

**Replication cycle failed with error "Permission to perform this operation was denied"**

This error occurs when the VMware account used to access the vCenter server from the Azure Migrate appliance, doesn't have sufficient permissions to replicate the virtual machine. Ensure that the account provided has the following VMware permissions:

- Datastore.Browse
- Datastore.LowLevelFileOperations
- VirtualMachine.Configuration.DiskChangeTracking
- VirtualMachine.Configuration.DiskLease
- VirtualMachine.Provisioning.AllowReadOnlyDiskAccess
- VirtualMachine.SnapshotManagement.* 
- VirtualMachine.Provisioning.AllowVirtualMachineDownload
- VirtualMachine.Interaction.PowerOff

You can update the account with one that has sufficient permissions by going to the [appliance management portal](https://appliance_ip_address:44368)

**Replication cycle failed with error "No disk snapshots were found for snapshot replication"**

This error occurs when a storage vMotion happens on a virtual machine under replication. Storage vMotion of a virtual machine under replication is currently not supported.

- Storage vMotion the virtual machine back to its original datastore to allow subsequent replication cycles to proceed
- Else, stop replication for the virtual machine and configure replication again. This is equivalent to a fresh replication of the virtual machine after the storage vMotion.

**Replication cycle failed with error "encountered an error while trying to fetch change blocks"**

* The agentless replication method uses VMware's changed block tracking technology(CBT) to optimize replication. CBT lets Server Migration track and replicate only the blocks that have changed since the last replication cycle. This error occurs if changed block tracking for a replicating virtual machine is reset or if the changed block tracking file is corrupt.
* If this error occurs, stop replication for the virtual machine, [reset changed block tracking](https://kb.vmware.com/s/article/1031873) on the virtual machine, and then reconfigure replication
* One such known issue that may cause a CBT reset of virtual machine on VMware vSphere 5.5 is described in
[VMware KB 2048201: Changed Block Tracking is reset after a storage vMotion operation in vSphere 5.x](https://kb.vmware.com/s/article/2048201). If you are on VMware vSphere 5.5 ensure that you apply the updates described in this KB.
* [Resetting VMware changed block tracking on a virtual machine using VMware PowerCLI](https://kb.vmware.com/s/article/1031873)

**Replication cycle failed with error "Snapshot Replication engine encountered timeout"**

This error occurs when the Azure Migrate Replication Gateway service component on the Azure Migrate appliance is unable to communicate with the Azure Migrate: Server Migration tool. Ensure that the appliance is powered on, has internet connectivity, and that the Azure Migrate Replication Gateway service is running (from run > services.msc)

If the Azure Migrate appliance is behind a proxy server, ensure that these URLs are whitelisted for access on the proxy server (including canonical name resolution of the URLs):

- *.portal.azure.com
- *.windows.net
- *.microsoftonline.com
- management.azure.com
- dc.services.visualstudio.com
- *.vault.azure.net
- *.servicebus.windows.net
- *.discoverysrv.windowsazure.com
- *.migration.windowsazure.com
- *.hypervrecoverymanager.windowsazure.com
- *.blob.core.windows.net

### Agent based replication of VMware virtual machines and physical servers

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

### Agentless replication of Hyper-V virtual machines

**Failures while attempting to replicate a Hyper-V virtual machine**

If you experience failures in the 'Start replication' operation, verify the following:

- Your Hyper-V hosts and VMs meet all [requirements and prerequisites](https://docs.microsoft.com/azure/migrate/migrate-support-matrix-hyper-v#migration-hyper-v-vm-requirements)
- The Hyper-V Virtual Machine Management service is running on Hyper-V hosts
- Look for Hyper-V-VMMS\Admin events in Event viewer on the virtual machine. This log is located in Applications and Services Logs > Microsoft > Windows
- If the virtual machine you are attempting to replicate is running Windows, ensure that WMI is enabled and accessible on the virtual machine
- [Learn about](https://blogs.technet.microsoft.com/askperf/2007/06/22/basic-wmi-testing/) basic WMI testing
- [Troubleshoot](https://docs.microsoft.com/windows/win32/wmisdk/wmi-troubleshooting) WMI
- [Troubleshoot](https://technet.microsoft.com/library/ff406382.aspx#H22) problems with WMI scripts and services
- Ensure that the latest version of Hyper-V Integration Services are running on the virtual machine
- [Check](https://docs.microsoft.com/windows-server/virtualization/hyper-v/manage/manage-hyper-v-integration-services) that you have the latest version of the integration services
- [Keep](https://docs.microsoft.com/windows-server/virtualization/hyper-v/manage/manage-hyper-v-integration-services#keep-integration-services-up-to-date) Integration Services up-to-date

**Replication issues**

Troubleshoot issues with initial and ongoing replication as follows:

- Verify whether replication is paused
- Check the VM health status in the Hyper-V Manager console
- If it's critical, right-click the VM > Replication > View Replication Health
- If replication is paused, click Resume Replication
- Ensure that the following services are running on the Hyper-V host:

    - Virtual Machine Management service
    - Microsoft Azure Recovery Services Agent service
    - Microsoft Azure Site Recovery service
    * WMI Provider Host service

- Check connectivity between the Hyper-V server and Azure. Specifically, check for connectivity to storage from the 'cbengine.exe' process (cbengine.exe is the name of the Windows process running on the Hyper-V server that performs the replication).
- To check connectivity, open Task Manager on the Hyper-V host. On the Performance tab, click Open Resource Monitor. On the Network tab go to "View TCP Connections" and select cbengine.exe by clicking the checkbox next to it. If connectivity exists, you'll see open connections between cbengine.exe and a URL resembling \*.blob.core.windows.net. This method will not work if the Hyper-V host has to go through a proxy server to connect to Azure.

**Replication health of the virtual machine is critical**

To check replication health, open Hyper-V manager on the Hyper-V host. Right click on the VM in the Hyper-V manager console, select 'Replication' and click 'View Replication Health'. If replication is paused, click 'Resume replication'.
