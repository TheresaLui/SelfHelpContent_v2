<properties
	pageTitle="Autorepair issue with my scale set"
	description="Autorepair issue with my scale set"
	service="microsoft.compute"
	resource=""
	authors="babhoo"
	ms.author="babhoo"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32740056"
	resourceTags=""
	productPesIds="16080"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="62d327f3-93e5-445d-bdfa-1c0d5b3c3e18"
	ownershipId="Compute_VirtualMachineScaleSets_Content"
/>

# Autorepair issue with my scale set

## **Recommended Steps**

For general troubleshooting, please follow these guides:<br>

1. For trouble while enabling feature, verify if scale set meets the [requirements](https://docs.microsoft.com/azure/virtual-machine-scale-sets/virtual-machine-scale-sets-automatic-instance-repairs#requirements-for-using-automatic-instance-repairs) for enabling Autorepair
2. For instances not getting repaired even when policy is enabled, review the [GracePeriod](https://docs.microsoft.com/azure/virtual-machine-scale-sets/virtual-machine-scale-sets-automatic-instance-repairs#grace-period) guidelines
3. [Verify the health status of an instance in a scale set](https://docs.microsoft.com/rest/api/compute/virtualmachinescalesetvms/getinstanceview)
4. Enabling [health monitoring](https://docs.microsoft.com/azure/virtual-machine-scale-sets/virtual-machine-scale-sets-health-extension) and [LoadBalancerProbes](https://docs.microsoft.com/azure/load-balancer/load-balancer-custom-probe-overview) for the scale set

### **Recommended Documents**

* [Automatic instance repairs for Azure virtual machine scale sets](https://docs.microsoft.com/azure/virtual-machine-scale-sets/virtual-machine-scale-sets-automatic-instance-repairs#requirements-for-using-automatic-instance-repairs)<br>
* [Instance Protection Policies](https://docs.microsoft.com/azure/virtual-machine-scale-sets/virtual-machine-scale-sets-instance-protection)<br>
* [Terminate notification for Azure virtual machine scale set instances](https://docs.microsoft.com/azure/virtual-machine-scale-sets/virtual-machine-scale-sets-terminate-notification)
