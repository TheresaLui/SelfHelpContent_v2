<properties
    pageTitle="Access Azure VMware Solution by CloudSimple - Portal" 
    description="Describes how to access VMware Solution by CloudSimple portal from Azure portal"
    infoBubbleText="Problems related to VMware VM performance on my Private Cloud"
    ms.service="azure-vmware-cloudsimple"
    authors="dikamath, sharaths-cs" 
    ms.author="dikamath, b-shsury, v-rabmah"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32637631"
    resourceTags=""
    productPesIds="16733"
    cloudEnvironments="public, fairfax, usnat, ussec" 
    articleId="a691d75f-9dcb-43cc-94d9-7d5a2260ecc4"    
	ownershipId="Compute_VirtualMachines_Content"
/>

# Troubleshooting virtual machine performance 

## **Recommended Steps**

<span title="Problems related to VMware VM performance on my Private Cloud">

* Check vCenter events for a disconnected or not responsive ESXi host
* Check vSAN Health tests for vSAN resync'ing components
* Check vSAN Performance stats for high congestion or I/O that is persistently higher than total disks I/O
* Check vSAN storage policy for better configuration. e.g. larger stripe width or a better RAID type
* Check network IO Control (NIOC) configuration
* Check for I/O overhead due to features in use e.g. vSAN encryption, vSAN Checksum
* Ensure that there are no backup activities during peak I/O
* Ensure that there are no virtual machine snapshot operation during peak I/O
* Check the guest OS file system 4KB alignment
* Ensure that Memory Trimming feature is disabled on I/O intensive virtual machines that are not memory intensive
* Check for active On-demand virus scan activities in the virtual machine
* If using SQL Server, check for optimization tips

</span>