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
    cloudEnvironments="public, Fairfax"
    articleId="75vc7598-2a3f-4d2d-96c5-b2b5886483e6"
	ownershipId="Compute_AzureMigrate"
/>

# Assessment recommendations

## **Recommended Steps**

### **Why is performance data missing for some VMs in my assessment report?**

The above issue is listed when the Azure Migrate appliance cannot collect performance data for the on-premises VMs. This can happen if:

- The VMs are powered off for the duration for which you are creating the assessment (last one day/one week/one month) as the appliance cannot collect performance data for a VM, when it is powered off
- If only memory counters are missing and you are trying to assess Hyper-V VMs, check if you have dynamic memory enabled on these VMs. There is a known issue currently due to which Azure Migrate appliance cannot collect memory utilization for VMs which do not have dynamic memory enabled. Note that the issue is only there for Hyper-V VMs and not there for VMware VMs. If any of the performance counters are missing, Azure Migrate: Server Assessment falls back to the allocated cores/memory and recommends a VM size accordingly.
- Outbound connections from the appliance on ports 5671 and 5672 is not being allowed

### **Why does Server Assessment mark my Linux VMs 'Conditionally ready'. Is there anything I need to do to fix this?**

There is a known gap in Server Assessment where it is unable to detect the minor version of the Linux OS installed on the on-premises VMs (for example, for RHEL 6.10, currently Server Assessment only detects RHEL 6 as the OS version). Since Azure endorses only specific versions of Linux, the Linux VMs are currently marked as conditionally ready in Server Assessment. We are working on this issue and this gap will be fixed in future. Meanwhile, you can manually ensure if the Linux OS running on the on-premises VM is endorsed in Azure by reviewing the [Azure Linux support documentation](https://docs.microsoft.com/azure/virtual-machines/linux/endorsed-distros). Once you have verified the endorsed distro, you can ignore this warning.

### **The VM SKU recommended by Server Assessment in an import-based assessment has less memory than what I have provided in my CSV. Why is that so?** 

This may happen due to the following reasons:
- You have provided the memory size in GB. The CSV expects the memory size to be in MB. 
- You have chosen a performance-based assessment and provided a memory utilization value that is lower than 100%.

### **The VM SKU recommended by Server Assessment has more number of cores and a larger memory size than what is allocated on-premises. Why is that so?**

The VM SKU recommendation in Server Assessment depends on the assessment properties. You can create two kinds of assessments in Server Assessment, 'performance-based' and 'as on-premises' assessments. For performance-based assessments, Server Assessment considers the utilization data of the on-premises VMs (CPU, memory, disk and network utilization) to determine the right target VM SKU for your on-premises VMs. Additionally, for performance-based sizing, the comfort factor is taken into account to identify the effective utilization. For as on-premises sizing, performance data is not considered and a target SKU is recommended based on what is allocated on-premises.

For example, let's say there is an on-premises VM with 4 cores and 8 GB memory with 50% CPU utilization and 50% memory utilization, and a comfort factor of 1.3 is specified in the assessment. If the sizing criterion of the assessment is 'As on-premises' an Azure VM SKU with 4 cores and 8 GB memory is recommended, however, if the sizing criterion is performance-based, based on effective CPU and memory utilization (50% of 4 cores * 1.3 = 2.6 cores and 50% of 8 GB memory * 1.3 = 5.3 GB memory), the cheapest VM SKU of 4 cores (nearest supported core count) and 8 GB memory size (nearest supported memory size) would be recommended. [Learn more about how Server Assessment performs sizing](https://docs.microsoft.com/azure/migrate/concepts-assessment-calculation#sizing).

### **The disk SKU recommended by Server Assessment has a bigger size than what is allocated on-premises. Why is that so?**

The disk sizing in Server Assessment depends on two assessment properties - sizing criterion and storage type. If the sizing criterion is 'Performance-based' and storage type is set to 'Automatic', the IOPS and throughput values of the disk are considered to identify the target disk type (Standard HDD, Standard SSD or Premium disks). A disk SKU within the disk type is then recommended considering the size requirements of the on-premises disk. If the sizing criterion is 'Performance-based' and storage type is 'Premium', a premium disk SKU in Azure is recommended based on the IOPS, throughput and size requirements of on-premises disk. The same logic is used to do disk sizing when the sizing criterion is 'As on-premises' sizing and storage type is 'Standard HDD', 'Standard SSD' or 'Premium'.

For example, if you have an on-premises disk with 32 GB memory, but the aggregated read and write IOPS for the disk is 800 IOPS, Server Assessment will recommend a premium disk type (due to the higher IOPS requirements) and then recommend a disk SKU which can support the required IOPS and size. The nearest match in this example would be P15 (256 GB, 1100 IOPS). So even though the size required by the on-premises disk was 32 GB, Server Assessment recommended a disk with bigger size due to the high IOPS requirement of the on-premises disk.

### **Why does my assessment report say 'PercentageOfCoresUtilizedMissing' or 'PercentageOfMemoryUtilizedMissing' for some VMs?**

The above issues are listed when the Azure Migrate appliance cannot collect performance data for the on-premises VMs. This can happen if the VMs are powered off for the duration for which you are creating the assessment (last one day/one week/one month) as the appliance cannot collect performance data for a VM, when it is powered off. If only memory counters are missing and you are trying to assess Hyper-V VMs, check if you have dynamic memory enabled on these VMs. There is a known issue currently due to which Azure Migrate appliance cannot collect memory utilization for VMs which do not have dynamic memory enabled. Note that the issue is only there for Hyper-V VMs and not there for VMware VMs. If any of the performance counters are missing, Azure Migrate: Server Assessment falls back to the allocated cores/memory and recommends a VM size accordingly.

### **Is the OS license cost of the VM included in the Compute cost estimated by Server Assessment?**

Server Assessment currently only considers the OS license cost for Windows machines, OS license cost for Linux machines is not considered currently. Support for Linux OS cost estimation is on our roadmap and will be enabled in future.

### **What impact does performance history and percentile utilization have on the size recommendations?**

These properties are only applicable for 'Performance-based' sizing. Server Assessment continuously collects performance data of on-premises machines and uses it to recommend the VM SKU and disk SKU in Azure. Below is how performance data is collected by Server Assessment:

- The Azure Migrate appliance continuously profiles the on-premises environment to gather real-time utilization data every 20 seconds for VMware VMs and every 30 seconds for Hyper-V VMs
- The appliance rolls up the 20/30-second samples to create a single data point for every 10 minutes. To create the single data point, the appliance selects the peak value from all the 20/30-second samples, and sends it to Azure.
- When you create an assessment in Server Assessment, based on the performance duration and performance history percentile value, the representative utilization value is identified. For example, if the performance history is 1 week and percentile utilization is 95th, Azure Migrate will sort all the 10-minute sample points for the last one week in ascending order and then select the 95th percentile as the representative value.

    The 95th percentile value ensures that you are ignoring any outliers, which may be included if you pick the 99th percentile. If you want to pick the peak usage for the period and do not want to miss any outliers, you should select 99th percentile as the percentile utilization.

### **Why is my VM marked not ready with 'One or more unsuitable disks'?**

The above values are listed when Azure Migrate detects an on-premises VM with disks that require high IOPS(greater than 20,000) which probably could not be met by non-ultra-disks. Currently, Azure Migrate currently does not support Ultra disks.

### Can I perform an application-based assessment using Server Assessment? 

No, currently Server Assessment offers only machine-level assessments for lift-and-shift migrations. However, you can run assessment of web applications and databases using the other [tools available in Azure Migrate](https://docs.microsoft.com/azure/migrate/migrate-services-overview#azure-tool-integration).