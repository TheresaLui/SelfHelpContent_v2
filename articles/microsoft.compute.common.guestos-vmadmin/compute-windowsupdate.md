<properties
    pageTitle="Windows Update Patch Issues"
    description="Windows Update Patch Issues"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="ScottAzure"
    ms.author="scotro"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32785642"
    resourceTags=""
    productPesIds="14749"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="32c9dddd-aa7b-470f-a489-a15f26bd8484"
    ownershipId="Compute_VirtualMachines_Content"
/>

# Troubleshoot Windows Update issues

4 out of 5 customers resolved their VM Windows Update issue using the steps below.<br>

## **Recommended Steps**

If you **don't** have access to your VM due to a reboot loop or other related issue, review these three articles:<br>
* [Azure VM startup is stuck at Windows Update](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-stuck-updating-boot-error)<br>
* [Azure VM is stuck in a reboot loop](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-reboot-loop)<br>
* [Troubleshoot Azure Virtual Machines boot issues](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/boot-error-troubleshoot)

If you **do** have access to your VM, use the following steps to troubleshoot the issue.<br>

### Step 1: Identify the issue by examining the event log for specific errors:

1. Open Event Viewer (from the **Control Panel** > **Administrative Tools**)<br>
2. Look for Windows Update Agent events in the System log, but also look for errors in the System and Application logs around the same time that updates were applied<br>
3. Expand the Event Viewer tree to **Application and Service Logs** > **Microsoft** > **Windows** > **WindowsUpdateClient** > **Operational**
4. Identify the Update that is failing to install and the failure code<br>
5. Find the error in [Common Windows Update errors](https://docs.microsoft.com/windows/deployment/update/windows-update-errors) or [Windows Update error codes by component](https://docs.microsoft.com/windows/deployment/update/windows-update-error-reference) and mitigate the issue, if possible


### Step 2: Run the Windows Update troubleshooter for Windows: 

1. Download the troubleshooter, and select **Open** or **Save** in the pop-up window. (If you chose **Save**, you'll need to open the troubleshooter from the save location.)<br>
2. Select **Next** to start the troubleshooter, and follow the steps to identify and fix any problems<br>
3. After the troubleshooter finishes, try running Windows Update again. From the **Start** button, select **Settings** > **Update & security** > **Windows Update** > **Check for updates**, and  install any available updates.
4. If applicable, [Reset windows update components](http://support.microsoft.com/kb/971058)

## **Recommended Documents**

* [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview)<br>
* [How to view VM reboot logs to identify the cause of reboot](https://azure.microsoft.com/blog/viewing-vm-reboot-logs)<br>
* [Diagnose and recover from boot failures after a restart](https://azure.microsoft.com/blog/boot-diagnostics-for-virtual-machines-v2/)<br>
* [Manage the availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/windows/manage-availability)<br>
* [Configure availability sets for virtual machines using Resource Manager deployments](https://docs.microsoft.com/azure/virtual-machines/windows/create-availability-set)<br>
* [Understand planned maintenance for virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/windows/maintenance-and-updates)<br>
* [Service Healing - Auto-recovery of Virtual Machines](https://azure.microsoft.com/blog/service-healing-auto-recovery-of-virtual-machines)<br>
* [Use Azure redeploy functionality to transfer virtual machines to a new Azure node](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/redeploy-to-new-node-windows)
