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
	cloudEnvironments="public"
	articleId="62d327f3-93e5-445d-bdfa-1c0d5b3c3e18"
	ownershipId="Compute_VirtualMachineScaleSets_Content"
/>

# Autorepair issue with my scale set

### **Awareness**

>We are currently experiencing high demand for specific regions. For further information, please review our [commitment to customers and Microsoft Cloud Services continuity](https://azure.microsoft.com/en-us/blog/update-2-on-microsoft-cloud-services-continuity/).<br>

## **Recommended Steps**

For general troubleshooting, please follow these guides:<br>

1. For trouble while enabling feature, verify if scale set meets the requirement for enabling Autorepair.([Requirements](https://docs.microsoft.com/azure/virtual-machine-scale-sets/virtual-machine-scale-sets-automatic-instance-repairs#requirements-for-using-automatic-instance-repairs))<br>
2. For instance not getting repaired even when policy is enabled. ([GracePeriod](https://docs.microsoft.com/azure/virtual-machine-scale-sets/virtual-machine-scale-sets-automatic-instance-repairs#grace-period))<br>
3. Verify the health status of an instance in a scale set([VerifyInstanceHealthy](https://docs.microsoft.com/rest/api/compute/virtualmachinescalesetvms/getinstanceview))<br>
4. Enabling health monitoring for the scale set([Health Extension](https://docs.microsoft.com/azure/virtual-machine-scale-sets/virtual-machine-scale-sets-health-extension),([LoadBalancerProbes](https://docs.microsoft.com/azure/load-balancer/load-balancer-custom-probe-overview))

### **Recommended Documents**

* [Automatic instance repairs for Azure virtual machine scale sets](https://docs.microsoft.com/azure/virtual-machine-scale-sets/virtual-machine-scale-sets-automatic-instance-repairs#requirements-for-using-automatic-instance-repairs)<br>
* [Instance Protection Policies](https://docs.microsoft.com/azure/virtual-machine-scale-sets/virtual-machine-scale-sets-instance-protection)<br>
* [Terminate notification for Azure virtual machine scale set instances](https://docs.microsoft.com/azure/virtual-machine-scale-sets/virtual-machine-scale-sets-terminate-notification) 

