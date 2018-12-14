<properties
	pageTitle="Assessment creation and updates in Azure Migrate"
	description="Issues and guidance regarding Assessment creation and updates in Azure Migrate"
	service="microsoft.migrate"
	resource="projects"
	authors="nsoneji"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32593684, 32593687, 32593692, 32593693"
	resourceTags=""
	productPesIds="16348"
	cloudEnvironments="public"
/>

# Assessment creation and updates in Azure Migrate

## **Recommended steps**

### **How can I customize an assessment?**
You can customize your assessment by changing the assessment properties. [Learn more](https://docs.microsoft.com/azure/migrate/how-to-modify-assessment) about how to edit the assessment properties.

### **How is Azure VM sizing determined by Azure Migrate?**
There are two ways you can configure your assessment to determine the best Azure VM size for your migration. The first is "performance-based" sizing. With this method, Azure Migrate will attempt to determine the best VM size for you based on the performance characteristics of your on-prem VM. The second method, "on-premises" sizing, does not take performance history into consideration and will select an Azure VM size for you that most closely matches that of your on-prem VM. [Learn more](https://docs.microsoft.com/azure/migrate/concepts-assessment-calculation#sizing) about how Azure Migrate determines the right Azure VM sizing.

### **Can I specify Enterprise Agreement (EA) subscriptions in assessment properties?**
No, Azure Migrate currently does not support Enterprise Agreement (EA) based offers. The workaround is to use a ‘Pay-As-You-Go’ offer and use the ‘Discount’ property to specify any custom discounts that you receive. [Learn more](https://docs.microsoft.com/azure/migrate/how-to-modify-assessment) about the configurable properties of an assessment.
