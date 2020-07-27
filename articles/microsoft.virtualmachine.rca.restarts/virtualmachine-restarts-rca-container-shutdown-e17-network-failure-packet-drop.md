<properties
	pageTitle="VMA RCA"
	description="RCA - Container shutdown - E17 Network Packet Drop Failure"
	infoBubbleText="Found recent reboot. See details on the right."
	service=""
	resource=""
	authors="NatErns"
	ms.author="naterns"
	displayOrder=""
	articleId="UnexpectedVMReboot_RCA-Container_shutdown-E17_Network_Failure_Packet_Drop"
	diagnosticScenario="UnexpectedVMReboot"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags="windows, linux"
	productPesIds=""
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We identified that your VM **<!--$vmname--> Virtual machine <!--/$vmname-->** became unavailable at **<!--$StartTime--> StartTime <!--/$StartTime--> (UTC)** and availability was restored at **<!--$EndTime--> EndTime <!--/$EndTime--> (UTC)**. This unexpected occurrence was caused by an **Azure initiated temporary VM shutdown**.
<!--/issueDescription-->

The physical node where the virtual machine was hosted experienced a **platform bug involving the NIC firmware and drivers used for the Accelerated Networking**. The bug causes sporadic drops in connectivity resulting in a loss of connectivity to storage accounts. 

Our engineering team is proactively applying a temporary mitigation to all affected nodes and actively rolling out a hotfix. 

We regret that this platform bug had an impact on your VM. The Azure engineering teams are investing in both short and long-term initiatives to prevent such incidents going forward.

We apologize for any inconvenience this may have caused you. We are continuously working to improve the platform to reduce incidences of virtual machine unavailability.
<br>

## **Recommended Steps**

To ensure an increased level of protection and redundancy for your application in Azure, we recommend that you group two or more virtual machines in an availability set.

## **Recommended Documents**

* [Manage the availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/windows/manage-availability)<br>
* [Configure availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/windows/tutorial-availability-sets)<br>
* [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview)<br>
