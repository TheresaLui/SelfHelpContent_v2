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

### **Why is performance data missing for some/all VMs in my assessment report?**

For "Performance-based" assessment, the assessment report export says 'PercentageOfCoresUtilizedMissing' or 'PercentageOfMemoryUtilizedMissing' when the Azure Migrate appliance cannot collect performance data for the on-premises VMs. Please check:

- If the VMs are powered on for the duration for which you are creating the assessment
- If only memory counters are missing and you are trying to assess Hyper-V VMs, check if you have dynamic memory enabled on these VMs. There is a known issue currently due to which Azure Migrate appliance cannot collect memory utilization for such VMs.
- If all of the performance counters are missing, ensure that outbound connections on ports 443 (HTTPS) is allowed.

Note- If any of the performance counters are missing, Azure Migrate: Server Assessment falls back to the allocated cores/memory on-premises and recommends a VM size accordingly.

### **Why is the confidence rating of my assessment low?**

The confidence rating is calculated for "Performance-based" assessments based on the percentage of [available data points](https://docs.microsoft.com/azure/migrate/concepts-assessment-calculation#ratings) needed to compute the assessment. Below are the reasons why an assessment could get a low confidence rating:

- You did not profile your environment for the duration for which you are creating the assessment. For example, if you are creating an assessment with performance duration set to one week, you need to wait for at least a week after you start the discovery for all the data points to get collected. If you cannot wait for the duration, please change the performance duration to a smaller period and 'Recalculate' the assessment.
 
- Server Assessment is not be able to collect the performance data for some or all the VMs in the assessment period. Please check if the VMs were powered on for the duration of the assessment, outbound connections on ports 443 are allowed. For Hyper-V VMs, if dynamic memory is enabled, memory counters will be missing leading to a low confidence rating. Please 'Recalculate' the assessment to reflect the latest changes in confidence rating. 

- Few VMs were created after discovery in Server Assessment had started. For example, if you are creating an assessment for the performance history of last one month, but few VMs were created in the environment only a week ago. In this case, the performance data for the new VMs will not be available for the entire duration and the confidence rating would be low.

[Learn more](https://docs.microsoft.com/azure/migrate/concepts-assessment-calculation#confidence-ratings-performance-based) about confidence rating.

### **My assessment is in "Outdated" state, why is that so?**

- If there are configuration changes (VM deletion, core addition/removal, memory size changes, boot type or firmware, OS, network adaptor, NIC changes- Mac address, IP address, disk addition/removal) in the on-premises environment for the VMs that are part of an assessment, Server Assessment marks the assessment as outdated. You can use the 'Recalculate' option in the assessment to update the assessment with latest changes.
- In case Dynamic memory has been enabled, it is likely that the assessment will be marked outdated when the memory counters change. The assessment is still usable, provided the difference in memory counter is not very big (which could change the SKU recommendations and cost).

## Azure VM assessment

### **Why does Server Assessment mark my Linux VMs 'Conditionally ready'. Is there anything I need to do to fix this?**

There is a known gap in Server Assessment where it is unable to detect the minor version of the Linux OS installed on the on-premises VMs (for example, for RHEL 6.10, currently Server Assessment only detects RHEL 6 as the OS version). This gap can be addressed by enabling application discovery on the VMware VMs. Server Assessment uses the operating system detected from the VM using the guest credentials provided.
Meanwhile, you can manually ensure if the Linux OS running on the on-premises VM is endorsed in Azure by reviewing the [Azure Linux support documentation](https://docs.microsoft.com/azure/virtual-machines/linux/endorsed-distros). Once you have verified the endorsed distro, you can ignore this warning.

### **The VM SKU recommended by Server Assessment in an import-based assessment has less memory than what I have provided in my CSV. Why is that so?**

This may happen due to the following reasons:

- You have provided the memory size in GB. The CSV expects the memory size to be in MB.
- You have chosen a performance-based assessment and provided a memory utilization value that is lower than 100%.

### **Readiness is 'Unknown OS' on my imported machine**
Ensure the operating system names provided in the CSV file meet the requirements documented [here](https://docs.microsoft.com/azure/migrate/tutorial-assess-import#supported-operating-system-names).


### **The VM SKU recommended by Server Assessment has more number of cores and a larger memory size than what is allocated on-premises. Why is that so?**

The VM SKU recommendation in Server Assessment depends on the assessment properties. You can create two kinds of assessments in Server Assessment, 'performance-based' and 'as on-premises' assessments. 
- For 'performance-based' assessments, Server Assessment considers the utilization data of the on-premises VMs (CPU, memory, disk, and network utilization) to determine the right target VM SKU for your on-premises VMs. It also adds a comfort factor when determining effective utilization.
- For 'as on-premises' assessments, performance data is not considered, and the target SKU is recommended based on-premises allocation.

For example, let's say there is an on-premises VM with 4 cores and 8 GB memory with 50% CPU utilization and 50% memory utilization, and a comfort factor of 1.3 is specified in the assessment:
- If the sizing criterion is 'As on-premises' an Azure VM SKU with 4 cores and 8 GB memory is recommended.
- If the sizing criterion is performance-based, based on effective CPU and memory utilization (50% of 4 cores *1.3 = 2.6 cores and 50% of 8 GB memory* 1.3 = 5.3 GB memory), the cheapest VM SKU of 4 cores (nearest supported core count) and 8 GB memory size (nearest supported memory size) would be recommended. [Learn more about how Server Assessment performs sizing](https://docs.microsoft.com/azure/migrate/concepts-assessment-calculation#calculating-sizing).

### **The disk SKU recommended by Server Assessment has a bigger size than what is allocated on-premises. Why is that so?**

The disk sizing in Server Assessment depends on two assessment properties - sizing criterion and storage type:
- If the sizing criterion is 'Performance-based' and storage type is set to 'Automatic', the IOPS and throughput values of the disk are considered to identify the target disk type (Standard HDD, Standard SSD or Premium disks). A disk SKU within the disk type is then recommended considering the size requirements of the on-premises disk. 
- If the sizing criterion is 'Performance-based' and storage type is 'Premium', a premium disk SKU in Azure is recommended based on the IOPS, throughput and size requirements of on-premises disk. The same logic is used to do disk sizing when the sizing criterion is 'As on-premises' sizing and storage type is 'Standard HDD', 'Standard SSD' or 'Premium'.

For example, if you have an on-premises disk with 32 GB memory, but the aggregated read and write IOPS for the disk is 800 IOPS, Server Assessment will recommend a premium disk type (due to the higher IOPS requirements) and then recommend a disk SKU which can support the required IOPS and size. The nearest match in this example would be P15 (256 GB, 1100 IOPS). So even though the size required by the on-premises disk was 32 GB, Server Assessment recommended a disk with bigger size due to the high IOPS requirement of the on-premises disk.

### **Is the OS license cost of the VM included in the Compute cost estimated in an Azure VM assessment?**

Server Assessment currently only considers the OS license cost for Windows machines, OS license cost for Linux machines is not considered currently. Support for Linux OS cost estimation is on our roadmap and will be enabled in future.

### **What impact does performance history and percentile utilization have on the size recommendations in an Azure VM assessment?**

These properties are only applicable for 'Performance-based' sizing. Server Assessment continuously collects performance data of on-premises machines and uses it to recommend the VM SKU and disk SKU in Azure. [Learn more](https://docs.microsoft.com/azure/migrate/concepts-assessment-calculation#how-does-the-appliance-calculate-performance-data) about how performance data is collected by Server Assessment. 

The 95th percentile value ensures that you are ignoring any outliers, which may be included if you pick the 99th percentile. If you want to pick the peak usage for the period and do not want to miss any outliers, you should select 99th percentile as the percentile utilization.

### **Why is my VM marked not ready with 'One or more unsuitable disks'?**

The above values are listed when Azure Migrate detects an on-premises VM with disks that require high IOPS(greater than 20,000) which probably could not be met by non-ultra-disks. Currently, Azure Migrate currently does not support Ultra disks.

### **Can I perform an application-based assessment using Server Assessment?**

No, currently Server Assessment offers only machine-level assessments for lift-and-shift migrations. However, you can run assessment of web applications and databases using the other [tools available in Azure Migrate](https://docs.microsoft.com/azure/migrate/migrate-services-overview#azure-tool-integration).

## Azure VMware Solution (AVS) assessment

### **How do I select FTT-RAID level in an AVS assessment?**

The storage engine used in Azure VMware Solution (AVS) is vSAN. vSAN storage polices define storage requirements for your virtual machines. These policies guarantee the required level of service for your VMs because they determine how storage is allocated to the VM. [Learn More](https://docs.microsoft.com/azure/migrate/concepts-azure-vmware-solution-assessment-calculation#ftt-sizing-parameters) about the available FTT-Raid combinations. 

### **How is node sizing done in an Azure VMware Solution (AVS) assessment?**

For sizing related queries, please refer to the documentation [here](https://docs.microsoft.com/azure/migrate/concepts-azure-vmware-solution-assessment-calculation#sizing)

### **Why is my VM marked conditionally ready Internet Protocol?**

AVS currently does not support IPv6 internet addressing. Contact your local MSFT AVS GBB team for guidance on remediation guidance if your machine is detected with IPv6.

### **Why can I not see some groups when I am creating an Azure VMware Solution (AVS) assessment?**

- AVS assessment can be done on groups that have only VMware machines. Please remove any non-VMware machine from the group if you intend to perform an AVS assessment.
- If you are running AVS assessments in Azure Migrate for the first time, it is advisable to create a new group of VMware machines.