<properties
	pageTitle="Machine discovery issues"
	description="Machine discovery issues"
	service="microsoft.migrate"
	resource="projects"
	authors="shijojoy"
	ms.author="shijoy"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32631901,32631933,32631932"
	resourceTags=""
	productPesIds="16348"
	cloudEnvironments="public"
	articleId="ecf87d57-c8c4-4009-8d82-f6d50af6c091"
/>

# Azure Migrate Machine discovery issues

## **Recommended Steps**

*  **I am using the OVA that continuously discovers my on-premises environment, but the VMs that are deleted in my on-premises environment are still being shown in the portal.**

	The continuous discovery appliance only collects performance data continuously, it does not detect any configuration change in the on-premises environment (i.e. VM addition, deletion, disk addition etc.). If there is a configuration change in the on-premises environment, you can do the following to reflect the changes in the portal:

	* Addition of items (VMs, disks, cores etc.): To reflect these changes in the Azure portal, you can stop the discovery from the appliance and then start it again. This will ensure that the changes are updated in the Azure Migrate project.
	* Deletion of VMs: Due to the way the appliance is designed, deletion of VMs is not reflected even if you stop and start the discovery. This is because data from subsequent discoveries are appended to older discoveries and not overridden. In this case, you can simply ignore the VM in the portal, by removing it from your group and recalculating the assessment.

* **Performance data for CPU, memory and disks is showing up as zeroes**

	Azure Migrate continuously profiles the on-premises environment to collect performance data of the on-premises VMs. If you have just started the discovery of your environment, you need to wait for at least a day for the performance data collection to be done. If an assessment is created without waiting for one day, the performance metrics will show up as zeroes. After waiting for a day, you can either create a new assessment or update the existing assessment by using the 'Recalculate' option in the assessment report.
