<properties
	pageTitle="Assessment creation and updates in Azure Migrate"
	description="Issues and guidance regarding Assessment creation and updates in Azure Migrate"
	service="microsoft.migrate"
	resource="projects"
	authors="nsoneji"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32593687"
	resourceTags=""
	productPesIds="16348"
	cloudEnvironments="public"
/>

# "Assessment creation and updates in Azure Migrate

## **Recommended steps**

### **How can I customize an assessment?**
You can customize your assessment by changing the assessment properties. [Learn more](https://docs.microsoft.com/azure/migrate/how-to-modify-assessment) about how to edit the assessment properties.

### **How is Azure VM sizing determined by Azure Migrate?**
There are two ways you can configure your assessment for right Azure VM size. You can do assessment based on either performance-based sizing or size the VMs as on-premises, without considering the performance history.
[Learn more](https://docs.microsoft.com/azure/migrate/concepts-assessment-calculation#sizing) Azure Migrate sizing.

3.	Can I specify EA subscriptions in assessment properties?
No, Azure Migrate currently does not support EA-based offers, the workaround is to use select ‘Pay-As-You-Go’ offer and use the ‘Discount’ property to specify any custom discounts. [Learn more] (https://docs.microsoft.com/en-us/azure/migrate/how-to-modify-assessment) these assessment properties. 
