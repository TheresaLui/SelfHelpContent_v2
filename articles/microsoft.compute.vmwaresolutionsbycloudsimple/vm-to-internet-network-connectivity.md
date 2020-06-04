<properties
    pageTitle="Access Azure VMware Solution by CloudSimple - Portal" 
    description="Describes how to access VMware Solution by CloudSimple portal from Azure portal"
    infoBubbleText="Problems related to internet access from VMs running in the Private Cloud"
    ms.service="azure-vmware-cloudsimple"
    authors="dikamath, sharaths-cs" 
    ms.author="dikamath, b-shsury, v-rabmah"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32637628"
    resourceTags=""
    productPesIds="16733"
    cloudEnvironments="public, fairfax, usnat, ussec" 
    articleId="b181aaef-75f4-4810-b37e-b03a74bc48b6"    
	ownershipId="Compute_VirtualMachines_Content"
/>

# Troubleshooting internet connectivity from a VM 

## **Recommended Steps**

* Check if there are firewall rules blocking any outbound traffic 
* Check the VM network configuration: IP address, subnet mask and gateway 
* Check if the VM is attached to correct distributed port group
* Check if the distributed port group has correct VLAN ID 

## **Recommended Documents**

<span title="Problems related to internet access from VMs running in the Private Cloud">

* [Use VLAN Information to Set Up a Distributed Port Group in vSphere](https://docs.microsoft.com/azure/vmware-cloudsimple/create-vlan-subnet#use-vlan-information-to-set-up-a-distributed-port-group-in-vsphere)<br>
</span>

<span title="Problems related to internet access from VMs running in the Private Cloud">

* [Firewall Rules](https://docs.microsoft.com/azure/vmware-cloudsimple/firewall#firewall-rules)<br>
</span>

<span title="Problems related to internet access from VMs running in the Private Cloud">

* [VLANs/Subnets](https://docs.microsoft.com/azure/vmware-cloudsimple/create-vlan-subnet)<br>
</span>