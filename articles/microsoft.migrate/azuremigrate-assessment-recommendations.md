<properties
    pageTitle="Assessment recommendations"
    description="Issues and guidance regarding assessment recommendations in Server Assessment"    service="microsoft.migrate"
    resource="migrateprojects"
    authors="snehaamicrosoft"
    ms.author="snehaa"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32675736"
    resourceTags=""
    productPesIds="16348"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="75vc7598-2a3f-4d2d-96c5-b2b5886483e6"
    ownershipId="Compute_AzureMigrate"
/>

# Assessment recommendations

## **Recommended Steps**

### **Why is performance data missing for some VMs in my assessment report?**

The assessment report says 'PercentageOfCoresUtilizedMissing' or 'PercentageOfMemoryUtilizedMissing' when the Azure Migrate appliance cannot collect performance data for the on-premises VMs. This can happen if:

- The VMs are powered off for the duration for which you are creating the assessment (last one day/one week/one month) as the appliance cannot collect performance data for a VM, when it is powered off
- If only memory counters are missing and you are trying to assess Hyper-V VMs, check if you have dynamic memory enabled on these VMs. There is a known issue currently due to which Azure Migrate appliance cannot collect memory utilization for VMs which do not have dynamic memory enabled. Note that the issue is only there for Hyper-V VMs and not there for VMware VMs. If any of the performance counters are missing, Azure Migrate: Server Assessment falls back to the allocated cores/memory and recommends a VM size accordingly.
- Outbound connections from the appliance on ports 5671 and 5672 is not being allowed
 
### **How do I choose the assessment type?**

- Use **Azure VM** assessments when you want to assess your on-premises VMware VMs, Hyper-V VMs, and physical servers for migration to Azure VMs. 
- Use **Azure VMware Solution (AVS)** assessments when you want to assess your on-premises VMware VMs for migration to [Azure VMware Solution (AVS)](https://docs.microsoft.com/azure/azure-vmware/introduction) using this assessment type. Azure VMware Solution (AVS) assessment is currently in Public Preview.
- You can use a common group with VMware machines only to run both types of assessments. Note that if you are running AVS assessments in Azure Migrate for the first time, it is advisable to create a new group of VMware machines.

## Azure VM assessment

### **Why does Server Assessment mark my Linux VMs 'Conditionally ready'. Is there anything I need to do to fix this?**

There is a known gap in Server Assessment where it is unable to detect the minor version of the Linux OS installed on the on-premises VMs (for example, for RHEL 6.10, currently Server Assessment only detects RHEL 6 as the OS version). Since Azure endorses only specific versions of Linux, the Linux VMs are currently marked as conditionally ready in Server Assessment. We are working on this issue and this gap will be fixed in future. Meanwhile, you can manually ensure if the Linux OS running on the on-premises VM is endorsed in Azure by reviewing the [Azure Linux support documentation](https://docs.microsoft.com/azure/virtual-machines/linux/endorsed-distros). Once you have verified the endorsed distro, you can ignore this warning.

### **The VM SKU recommended by Server Assessment in an import-based assessment has less memory than what I have provided in my CSV. Why is that so?**

This may happen due to the following reasons:

- You have provided the memory size in GB. The CSV expects the memory size to be in MB.
- You have chosen a performance-based assessment and provided a memory utilization value that is lower than 100%.

### **Readiness is 'Unknown OS' on my imported machine**
Ensure the operating system names provided in the CSV file meet the requirements documented [here](https://docs.microsoft.com/azure/migrate/tutorial-assess-import#supported-operating-system-names).


### **The VM SKU recommended by Server Assessment has more number of cores and a larger memory size than what is allocated on-premises. Why is that so?**

The VM SKU recommendation in Server Assessment depends on the assessment properties. You can create two kinds of assessments in Server Assessment, 'performance-based' and 'as on-premises' assessments. For performance-based assessments, Server Assessment considers the utilization data of the on-premises VMs (CPU, memory, disk and network utilization) to determine the right target VM SKU for your on-premises VMs. Additionally, for performance-based sizing, the comfort factor is taken into account to identify the effective utilization. For as on-premises sizing, performance data is not considered and a target SKU is recommended based on what is allocated on-premises.

For example, let's say there is an on-premises VM with 4 cores and 8 GB memory with 50% CPU utilization and 50% memory utilization, and a comfort factor of 1.3 is specified in the assessment. If the sizing criterion of the assessment is 'As on-premises' an Azure VM SKU with 4 cores and 8 GB memory is recommended, however, if the sizing criterion is performance-based, based on effective CPU and memory utilization (50% of 4 cores *1.3 = 2.6 cores and 50% of 8 GB memory* 1.3 = 5.3 GB memory), the cheapest VM SKU of 4 cores (nearest supported core count) and 8 GB memory size (nearest supported memory size) would be recommended. [Learn more about how Server Assessment performs sizing](https://docs.microsoft.com/azure/migrate/concepts-assessment-calculation#sizing).

### **The disk SKU recommended by Server Assessment has a bigger size than what is allocated on-premises. Why is that so?**

The disk sizing in Server Assessment depends on two assessment properties - sizing criterion and storage type. If the sizing criterion is 'Performance-based' and storage type is set to 'Automatic', the IOPS and throughput values of the disk are considered to identify the target disk type (Standard HDD, Standard SSD or Premium disks). A disk SKU within the disk type is then recommended considering the size requirements of the on-premises disk. If the sizing criterion is 'Performance-based' and storage type is 'Premium', a premium disk SKU in Azure is recommended based on the IOPS, throughput and size requirements of on-premises disk. The same logic is used to do disk sizing when the sizing criterion is 'As on-premises' sizing and storage type is 'Standard HDD', 'Standard SSD' or 'Premium'.

For example, if you have an on-premises disk with 32 GB memory, but the aggregated read and write IOPS for the disk is 800 IOPS, Server Assessment will recommend a premium disk type (due to the higher IOPS requirements) and then recommend a disk SKU which can support the required IOPS and size. The nearest match in this example would be P15 (256 GB, 1100 IOPS). So even though the size required by the on-premises disk was 32 GB, Server Assessment recommended a disk with bigger size due to the high IOPS requirement of the on-premises disk.

### **Is the OS license cost of the VM included in the Compute cost estimated in an Azure VM assessment?**

Server Assessment currently only considers the OS license cost for Windows machines, OS license cost for Linux machines is not considered currently. Support for Linux OS cost estimation is on our roadmap and will be enabled in future.

### **What impact does performance history and percentile utilization have on the size recommendations in an Azure VM assessment?**

These properties are only applicable for 'Performance-based' sizing. Server Assessment continuously collects performance data of on-premises machines and uses it to recommend the VM SKU and disk SKU in Azure. Below is how performance data is collected by Server Assessment:

- The Azure Migrate appliance continuously profiles the on-premises environment to gather real-time utilization data every 20 seconds for VMware VMs and every 30 seconds for Hyper-V VMs
- The appliance rolls up the 20/30-second samples to create a single data point for every 10 minutes. To create the single data point, the appliance selects the peak value from all the 20/30-second samples, and sends it to Azure.
- When you create an assessment in Server Assessment, based on the performance duration and performance history percentile value, the representative utilization value is identified. For example, if the performance history is 1 week and percentile utilization is 95th, Azure Migrate will sort all the 10-minute sample points for the last one week in ascending order and then select the 95th percentile as the representative value.

    The 95th percentile value ensures that you are ignoring any outliers, which may be included if you pick the 99th percentile. If you want to pick the peak usage for the period and do not want to miss any outliers, you should select 99th percentile as the percentile utilization.

### **Why is my VM marked not ready with 'One or more unsuitable disks'?**

The above values are listed when Azure Migrate detects an on-premises VM with disks that require high IOPS(greater than 20,000) which probably could not be met by non-ultra-disks. Currently, Azure Migrate currently does not support Ultra disks.

### **Can I perform an application-based assessment using Server Assessment?**

No, currently Server Assessment offers only machine-level assessments for lift-and-shift migrations. However, you can run assessment of web applications and databases using the other [tools available in Azure Migrate](https://docs.microsoft.com/azure/migrate/migrate-services-overview#azure-tool-integration).

### **Why can I not see certain SKUs in the assessment recommendation for Azure Government?**

The VM size recommendations in assessments for Azure Government will use the VM series specifically for Government Cloud regions. Comparison of Government SKUs with respect to public cloud SKUs can be found [here](https://azure.microsoft.com/global-infrastructure/services/?regions=usgov-non-regional%2Cus-dod-central%2Cus-dod-east%2Cusgov-arizona%2Cusgov-iowa%2Cusgov-texas%2Cusgov-virginia&products=virtual-machines) by selecting region as Azure Government.


## Azure VMware Solution (AVS) assessment

### **Why can I not see some groups when I am creating an Azure VMware Solution (AVS) assessment?**

- AVS assessment can be done on groups that have only VMware machines. Please remove any non-VMware machine from the group if you intend to perform an AVS assessment.
- If you are running AVS assessments in Azure Migrate for the first time, it is advisable to create a new group of VMware machines.

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