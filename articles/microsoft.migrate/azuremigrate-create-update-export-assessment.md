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
    cloudEnvironments="public"
    articleId="75vc5643-2a3f-4d0d-96c5-b2b6546483e6"
/>

# Creating, updating and exporting assessments

## **Recommended Steps**

### **Does Azure Migrate: Server Assessment support creation of assessments for physical servers?**

Server Assessment currently supports assessment of VMware and Hyper-V VMs, support for physical servers is currently not available and will be enabled in future. 

### **Why is the confidence rating of my assessment low?**

The confidence rating of an assessment helps you estimate the reliability of the recommendations provided by Azure Migrate: Server Assessment. It is calculated based on the availability of data points needed to compute the assessment. Below are the reasons why an assessment could get a low confidence rating:

- You did not profile your environment for the duration for which you are creating the assessment. For example, if you are creating a performance-based assessment with performance duration set to one week, you need to wait for at least a week after you start the discovery for all the data points to get collected. You can always click on 'Recalculate' to see the latest applicable confidence rating. Note that confidence rating is applicable only when you create a "Performance-based" assessment.

- Few VMs were shut down during the period for which the assessment is calculated. If some VMs were powered off for some duration, Server Assessment will not be able to collect the performance data for that period.

- Few VMs were created after discovery in Server Assessment had started. For example, if you are creating an assessment for the performance history of last one month, but few VMs were created in the environment only a week ago. In this case, the performance data for the new VMs will not be available for the entire duration and the confidence rating would be low.

[Learn more](https://aka.ms/migrate/confidencerating) about confidence rating.

### **My assessment is in "Outdated" state, why is that so?**

If there are configuration changes (VM deletion, core addition/removal, memory size changes, NIC changes, disk addition/removal) in the on-premises environment for the VMs that are part of an assessment, Server Assessment marks the assessment as outdated. You can use the 'Recalculate' option in the assessment to update the assessment with latest changes.

### **Can I customize an assessment after I have created it?**

Yes, you can customize assessments either while creating them or after they are created by using the 'Edit properties' option in the assessment. [Learn more](https://aka.ms/migrate/selfhelp/customizeplan) about the customization options in an assessment.
