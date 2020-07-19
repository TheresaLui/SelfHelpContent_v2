<properties
    pageTitle="Access Azure VMware Solution by CloudSimple - Portal" 
    description="Describes how to access VMware Solution by CloudSimple portal from Azure portal"
    infoBubbleText="Problems related to NSX on my Private Cloud"
    ms.service="azure-vmware-cloudsimple"
    authors="dikamath, sharaths-cs" 
    ms.author="dikamath, b-shsury, v-rabmah"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32637637"
    resourceTags=""
    productPesIds="16733"
    cloudEnvironments="public, fairfax, usnat, ussec" 
    articleId="b6228786-6cec-4a7d-89f4-fb03bfd683a8"    
	ownershipId="Compute_VirtualMachines_Content"
/>

# Troubleshooting virtual machineware NSX 

## **Recommended Steps**

<span title="Problems related to NSX on my Private Cloud">

* Check that the distributed logical router (DLR) is created for the user defined route (UDR)
* Check that the DLR internal interface is attached to source subnet that needs UDR
* Check that the DLR **internal** interface's IP address and subnet prefix length is the same as the source subnet that needs UDR
* Check that the DLR has an uplink interface
* Check that the DLR interface is attached to the port group to which the virtual appliance or the next-hop is attached
* Check that the DLR **uplink** interface's IP address and subnet prefix length is the same as the source subnet that needs UDR
* Check that the DLR's default gateway IP address is correct
* Check that the DLR's static route for destination subnet exists and is configured correctly
* Check that NSX distributed switch is not preventing communication between source and destination
* Check if the destination virtual machine is attached to a DLR(UDR) which is blackholing traffic for the return traffic
* Check that the Source/Destination virtual machine is attached to the correct port group
* Check that the Source/Destination virtual machine IP, subnet mask and Default Gateway are configured correctly
* Check if the virtual machine's OS Firewall rules block the traffic
* Check that the virtual appliance has IP forwarding enabled or has proper routes

</span>
