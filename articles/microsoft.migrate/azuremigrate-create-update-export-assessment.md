<properties
    pageTitle="Creating, updating and exporting assessments"
    description="Issues and guidance regarding creating, updating and exporting assessments"
    service="microsoft.migrate"
    resource="migrateprojects"
    authors="snehaamicrosoft"
    ms.author="snehaa"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32675741"
    resourceTags=""
    productPesIds="16348"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="75vc5643-2a3f-4d0d-96c5-b2b6546483e6"
	ownershipId="Compute_AzureMigrate"
/>

# Creating, updating and exporting assessments

## **Recommended Steps**

### **Why is the confidence rating of my assessment low?**

The confidence rating of an assessment helps you estimate the reliability of the recommendations provided by Azure Migrate: Server Assessment. It is calculated based on the availability of data points needed to compute the assessment. Below are the reasons why an assessment could get a low confidence rating:

- You did not profile your environment for the duration for which you are creating the assessment. For example, if you are creating a performance-based assessment with performance duration set to one week, you need to wait for at least a week after you start the discovery for all the data points to get collected. You can always click on 'Recalculate' to see the latest applicable confidence rating. Note that confidence rating is applicable only when you create a "Performance-based" assessment.

- Few VMs were shut down during the period for which the assessment is calculated. If some VMs were powered off for some duration, Server Assessment will not be able to collect the performance data for that period.

- Few VMs were created after discovery in Server Assessment had started. For example, if you are creating an assessment for the performance history of last one month, but few VMs were created in the environment only a week ago. In this case, the performance data for the new VMs will not be available for the entire duration and the confidence rating would be low.

[Learn more](https://docs.microsoft.com/azure/migrate/concepts-assessment-calculation#confidence-ratings-performance-based) about confidence rating.


### **How do I choose the assessment type?**

- Use **Azure VM** assessments when you want to assess your on-premises VMware VMs, Hyper-V VMs, and physical servers for migration to Azure VMs. 
- Use **Azure VMware Solution (AVS)** assessments when you want to assess your on-premises VMware VMs for migration to [Azure VMware Solution (AVS)](https://docs.microsoft.com/azure/azure-vmware/introduction) using this assessment type. Azure VMware Solution (AVS) assessment is currently in Public Preview.
- You can use a common group with VMware machines only to run both types of assessments. Note that if you are running AVS assessments in Azure Migrate for the first time, it is advisable to create a new group of VMware machines.

### **Why can I not see some groups when I am creating an Azure VMware Solution (AVS) assessment?**

- AVS assessment can be done on groups that have only VMware machines. Please remove any non-VMware machine from the group if you intend to perform an AVS assessment.
- If you are running AVS assessments in Azure Migrate for the first time, it is advisable to create a new group of VMware machines.

### **My assessment is in "Outdated" state, why is that so?**

- If there are configuration changes (VM deletion, core addition/removal, memory size changes, boot type or firmware, OS, network adaptor, NIC changes- Mac address, IP address, disk addition/removal) in the on-premises environment for the VMs that are part of an assessment, Server Assessment marks the assessment as outdated. You can use the 'Recalculate' option in the assessment to update the assessment with latest changes.
- In case Dynamic memory has been enabled, it is likely that the assessment will be marked outdated when the memory counters change. The assessment is still usable, provided the difference in memory counter is not very big (which could change the SKU recommendations and cost).

### **Can I customize an assessment after I have created it?**

Yes, you can customize assessments either while creating them or after they are created by using the 'Edit properties' option in the assessment. [Learn more](https://docs.microsoft.com/azure/migrate/how-to-modify-assessment) about the customization options in an assessment.

### **Why does my assessment report say 'PercentageOfCoresUtilizedMissing' or 'PercentageOfMemoryUtilizedMissing' for some VMs?**

The above issue is listed when the Azure Migrate appliance cannot collect performance data for the on-premises VMs. This can happen if:

- The VMs are powered off for the duration for which you are creating the assessment (last one day/one week/one month) as the appliance cannot collect performance data for a VM, when it is powered off
- If only memory counters are missing and you are trying to assess Hyper-V VMs, check if you have dynamic memory enabled on these VMs. There is a known issue currently due to which Azure Migrate appliance cannot collect memory utilization for VMs which do not have dynamic memory enabled. Note that the issue is only there for Hyper-V VMs and not there for VMware VMs. If any of the performance counters are missing, Azure Migrate: Server Assessment falls back to the allocated cores/memory and recommends a VM size accordingly.
- Outbound connections from the appliance on ports 5671 and 5672 is not being allowed

### **How do I select FTT-RAID level in an AVS assessment?**

The storage engine used in Azure VMware Solution (AVS) is vSAN. vSAN storage polices define storage requirements for your virtual machines. These policies guarantee the required level of service for your VMs because they determine how storage is allocated to the VM. These are the available FTT-Raid Combinations: 

**Failures to Tolerate (FTT)** | **RAID Configuration** | **Minimum Hosts Required** | **Sizing consideration**
--- | --- | --- | --- 
1 | RAID-1 (Mirroring) | 3 | A 100GB VM would consume 200GB.
1 | RAID-5 (Erasure Coding) | 4 | A 100GB VM would consume 133.33GB
2 | RAID-1 (Mirroring) | 5 | A 100GB VM would consume 300GB.
2 | RAID-6 (Erasure Coding) | 6 | A 100GB VM would consume 150GB.
3 | RAID-1 (Mirroring) | 7 | A 100GB VM would consume 400GB.

### **What is the suggested tool for migration to Azure VMware Solution (AVS)?**

In the Azure readiness report for Azure VMware Solution (AVS) assessment, you can see the following suggested tools:
- **VMware HCX or Enterprise**: For VMware machines, VMWare Hybrid Cloud Extension (HCX) solution is the suggested migration tool to migrate your on-premises workload to your Azure VMWare Solution (AVS) private cloud. [Learn More](https://docs.microsoft.com/azure/azure-vmware/hybrid-cloud-extension-installation).
- **Unknown**: For machines imported via a CSV file, the default migration tool is unknown. Though for VMware machines, it is recommended to use the VMWare Hybrid Cloud Extension (HCX) solution.

### **How is node sizing done in an  Azure VMware Solution (AVS) assessment?**

- **Storage sizing**: Server Assessment uses the total on-premises VM disk space and the Failures to tolerate setting to determine the vSAN storage required in the AVS nodes. IOPS and throughput of the VM disks is not used in storage calculations.
- **Compute sizing**: After it calculates storage requirements, Server Assessment considers CPU and memory requirements of the virtual machines, and teh comfort factor applied to determine the number of nodes required for AVS based on the node type. Currently by default, hyperthreading is enabled and thus a 36 core nodes will have 72 vCores. 4 vCores per physical is used to determine CPU thresholds per cluster using the VMware standard of not exceeding 80% utilization to allow for maintenance or failures to be handled without compromising cluster availability.
- **Network sizing**: Server Assessment currently does not take any network settings into consideration for AVS Assessments.

### **Why is my VM marked conditionally ready Internet Protocol?**

AVS currently does not support IPv6 internet addressing. Contact your local MSFT AVS GBB team for guidance on remediation guidance if your machine is detected with IPv6.