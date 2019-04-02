<properties
	pageTitle="Assessment recommendations in Azure Migrate"
	description="Issues and guidance regarding assessment recommendations in Azure Migrate"
	service="microsoft.migrate"
	resource="projects"
	authors="snehaamicrosoft"
	ms.author="snehaa"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32631921"
	resourceTags=""
	productPesIds="16348"
	cloudEnvironments="public"
	articleId="75be4298-2a3f-4d0d-96c5-b2b5886483e6"
/>

# Assessment creation and updates in Azure Migrate

## **Recommended steps**

### **Can I specify Enterprise Agreement (EA) as an Azure offer in assessment properties?**
No, Azure Migrate currently does not support Enterprise Agreement (EA) based offers. The workaround is to use a ‘Pay-As-You-Go’ offer and use the ‘Discount’ property to specify any custom discounts that you receive. [Learn more about the configurable properties of an assessment](https://docs.microsoft.com/azure/migrate/how-to-modify-assessment).

### **Is the OS cost of the VM included in the Compute cost estimated by Azure Migrate?**
Azure Migrate currently only considers the OS cost for Windows machines, OS license cost for Linux machines is not considered currently. Support for Linux OS cost estimation is in the roadmap and will be enabled in future.

### **I have a Linux VM with an OS that is endorsed in Azure, but Azure Migrate is still marking it as conditionally ready, is there anything I need to do to fix this?**
There is a known gap in Azure Migrate where it does not detect the minor version of the Linux OS installed (for example, for RHEL 6.10, it will only detect RHEL 6), which is why almost all Linux OSes are marked as conditionally ready (the condition being the minor version of the OS should be above a certain version). This issue will be fixed in the next releases. Meanwhile, you can manually ensure if the Linux OS in the on-premises VM is endorsed in Azure by reviewing the [Azure Linux support documentation](https://docs.microsoft.com/azure/virtual-machines/linux/endorsed-distros).

### **How is Azure VM sizing determined by Azure Migrate?**
There are two ways you can configure your assessment to determine the best Azure VM size for your migration. The first is "performance-based" sizing. With this method, Azure Migrate will attempt to determine the best VM size for you based on the performance characteristics of your on-prem VM. The second method, "on-premises" sizing, does not take performance history into consideration and will select an Azure VM size for you that most closely matches that of your on-prem VM. For example, if there is an on-premises VM with 4 cores and 8-GB memory with 50% CPU utilization and 50% memory utilization. If the sizing criterion is as on-premises sizing an Azure VM SKU with 4 cores and 8-GB memory is recommended, however, if the sizing criterion is performance-based as VM SKU of 2 cores and 4 GB would be recommended as the utilization percentage is considered while recommending the size. [Learn more about how Azure Migrate determines the right Azure VM sizing](https://docs.microsoft.com/azure/migrate/concepts-assessment-calculation#sizing).

### **How is disk sizing done in Azure Migrate?**
The disk sizing for Azure depends on two assessment properties - sizing criterion and storage type. If the sizing criterion is performance-based and storage type is automatic, the IOPS and throughput values of the disk are considered to identify the target disk type (Standard or Premium). If the sizing criterion is performance-based and storage type is premium, a premium disk is recommended, the premium disk SKU in Azure is selected based on the size of the on-premises disk. The same logic is used to do disk sizing when the sizing criterion is as on-premises sizing and storage type is standard or premium.

### **What impact does performance history and percentile utilization have on the size recommendations?**
These properties are only applicable for performance-based sizing. Azure Migrate collects performance history of on-premises machines and uses it to recommend the VM size and disk type in Azure.

- The collector appliance continuously profiles the on-premises environment to gather real-time utilization data every 20 seconds.
- The appliance rolls up the 20-second samples, and creates a single data point for every 15 minutes. To create the single data point, the appliance selects the peak value from all the 20-second samples, and sends it to Azure.
- When you create an assessment in Azure, based on the performance duration and performance history percentile value, Azure Migrate calculates the effective utilization value and uses it for sizing.

For example, if you have set the performance duration to be 1 day and percentile value to 95 percentile, Azure Migrate uses the 15-min sample points sent by collector for the last one day, sorts them in ascending order and picks the 95th percentile value as the effective utilization. The 95th percentile value ensures that you are ignoring any outliers, which may come if you pick the 99th percentile. If you want to pick the peak usage for the period and do not want to miss any outliers, you should select the 99th percentile.
