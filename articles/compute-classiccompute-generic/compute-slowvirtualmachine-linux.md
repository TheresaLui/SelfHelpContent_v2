<properties
	pageTitle="performance/slow virtual machine"
	description="performance/slow virtual machine"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="ScottAzure,timbasham"
	ms.author="scotro,tibasham"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32628264,32628261,32628277,32628275,32628268,32628270"
	resourceTags=""
	productPesIds="15571,16342,15797,16454,16470"
	cloudEnvironments="public"
	articleId="144af4cf-13a4-4575-8832-06b7c53c433f"
/>

# My VM is slow

4 out of 5 customers resolved their performance issue using the below steps.<br>

## **Recommended Steps**

1. Review your application error logs, traces, and metrics to determine if any application level bottlenecks are causing performance issues. As a quick way to recover from one-time issues, restart your application and virtual machine.
2. Review operating system level metrics such as CPU, memory usage, IO, and network to see if any resource has consistently high utilization

	* Use commands such as Top, VmStat, Lsof, and Tcpdump

3. Use VM Diagnostics and Storage Diagnostics in the Azure portal to identify if any resource is being overutilized or throttled
4. [Enable diagnostics, monitor, identify and remediate issues with Azure VMs and storage](https://support.microsoft.com/help/3150851/generic-performance-troubleshooting-for-azure-virtual-machine-running)
5. Address any Azure host issues by [redeploying](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/redeploy-to-new-node-linux#use-the-azure-portal) the VM, which migrates it to a new Azure host
6. Scale up the Virtual Machine to a different VM type or series for increased performance by clicking 'Size' in the Settings blade of the VM resource
7. Consider using [Premium Storage: High-Performance Storage for Azure Virtual Machine Workloads](https://docs.azure.cn/storage/storage-premium-storage/) if its an I/O intensive use-case 

## **Recommended Documents**

* [Scalability and performance targets for VM disks on Linux](https://docs.microsoft.com/azure/virtual-machines/linux/disk-scalability-targets)<br>
* [High-performance Premium Storage and managed disks for VM](https://docs.microsoft.com/azure/virtual-machines/windows/premium-storage)<br>
* [Optimize your Linux VM on Azure](https://docs.microsoft.com/azure/virtual-machines/linux/optimization)<br>
* [Tutorial: Monitor and update a Linux virtual machine in Azure](https://docs.microsoft.com/azure/virtual-machines/linux/tutorial-monitoring)<br>
* [Azure Premium Storage: Design for High Performance](https://docs.microsoft.com/azure/virtual-machines/linux/premium-storage-performance)<br>
* [Configure VMs for optimal Storage performance](https://blogs.msdn.microsoft.com/mast/2014/10/14/configuring-azure-virtual-machines-for-optimal-storage-performance/)
