<properties 
    pageTitle="Dependency Visualization"
    description="Issues and guidance regarding view dependencies feature in Azure Migrate: Server Assessment"
    service="microsoft.migrate"
    resource="migrateprojects"
    authors="musa-57"
    ms.author="hamusa"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32675744"
    resourceTags=""
    productPesIds="16348"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="b5dcb587-3130-4550-af8e-2517b61fb5e2"
	ownershipId="Compute_AzureMigrate"
/>

# View Dependencies

## **Recommended Steps**

### **I want to configure Azure Migrate: Server Assessment to use an existing OMS workspace. How do I do that?**

When you configure your OMS workspace for the first time for an Azure Migrate: Server Assessment project, you can either create a new or use an existing OMS workspace. [Learn more](https://go.microsoft.com/fwlink/?linkid=2104261) about how to configure an OMS workspace in Server Assessment.

### I am not able to create an Log Analytics workspace in the region of my preference. How do I proceed?

Azure Migrate currently supports creation of OMS workspace in East US, Southeast Asia and West Europe regions. Within Azure Migrate, you cannot create a workspace in regions in Japan or Australia. Even if the workspace is created outside of Azure Migrate in an unsupported region, it currently cannot be associated with an Azure Migrate project. This limitation is temporary and will be addressed in the future.

### I am not able to associate my Log Analytics workspace with the Azure Migrate project. How do I proceed?

Azure Migrate currently supports creation or associations of OMS workspaces that are in East US, Southeast Asia and West Europe regions. Within Azure Migrate, you cannot create a workspace in regions in Japan or Australia. Even if the workspace is created outside of Azure Migrate in an unsupported region, it currently cannot be associated with an Azure Migrate project. This limitation is temporary and will be addressed in the future.

### **Can I change the OMS workspace used by Server Assessment?**

No, you cannot change the OMS workspace once it has been configured.

### ***What is the supported OS matrix for the Microsoft Monitoring Agent (MMA) and the dependency agent?***

Refer to the support matrix document [MMA agent](https://go.microsoft.com/fwlink/?linkid=2104194) and [dependency agent](https://go.microsoft.com/fwlink/?linkid=2104195) for details.

### **I want to automate the installation of Microsoft Monitoring Agent (MMA) and dependency agent. How do I do that?**

You can use scripts to deploy the [dependency](https://go.microsoft.com/fwlink/?linkid=2104389) and [MMA](https://go.microsoft.com/fwlink/?linkid=2104390) agents. You can also leverage deployment tools such as System Center Configuration Manager (SCCM) and [Intigua](https://go.microsoft.com/fwlink/?linkid=2104196) to deploy the agents. The MMA agent can also be installed using this [script](https://go.microsoft.com/fwlink/?linkid=2104394).

### ***I installed agents on my on-premises VMs, but the dependencies are not showing up. What should I do?***

Typically, the dependencies start showing up after 15-20 minutes of installing the agents. [Learn more about agent installation](https://go.microsoft.com/fwlink/?linkid=2104392).

### **Do I need to install Service Map agents if I have System Center Operations Manager set up already?**

For machines monitored by System Center Operations Manager 2012 R2 or later, there is no need to install the MMA agent. Service Map has an integration with SCOM that leverages the SCOM MMA to gather the necessary dependency data. You can enable the integration using the guidance [here](https://go.microsoft.com/fwlink/?linkid=2104197). Note that the dependency agent will still need to be installed on these machines.

### **Is dependency visualization supported for groups with more than 10 VMs?**

You can visualize dependencies of groups with up to 10 VMs. However, you can use Azure Monitor logs to [query the dependency data](https://go.microsoft.com/fwlink/?linkid=2104393) in a tabular format for any number of VMs. If you are only looking to visualize dependencies, we recommend you split the group into smaller groups and visualize dependencies.

### **Can I visualize dependencies for more than one-hour duration?**

No, Server Assessment lets you visualize dependencies for up to one-hour. You can go back to any specific date in the last one month, but the duration for which you can visualize the dependencies is up to one-hour. However, you can use Azure Monitor logs to [query the dependency data](https://go.microsoft.com/fwlink/?linkid=2104393) in a tabular format over a longer duration.

### **I want to retrieve connection port and data volume information using Service Map. How do I do that?**

TCP connection port and data volume information can be retrieved by running Log Analytics queries. Find information on sample queries and how they can be run [here](https://go.microsoft.com/fwlink/?linkid=2104393)

### **Can I export the dependency visualization report?**

No, currently you cannot export the dependency visualization report. However, we are working on adding support for it. 
For now, you can retrieve dependency information by running Log Analytics queries. Find information on sample queries and how they can be run [here](https://go.microsoft.com/fwlink/?linkid=2104393)

### ***Is there a charge for using dependency visualization?***

• The [Service Map solution](https://go.microsoft.com/fwlink/?linkid=2104198) will not incur any charges for the first 180 days from the day of associating the [Log Analytics](https://go.microsoft.com/fwlink/?linkid=2104198) workspace with Server Assessment. After 180 days, standard Log Analytics charges will apply.

• The use of any solution other than Service Map within the linked OMS workspace will incur standard [Log Analytics](https://go.microsoft.com/fwlink/?linkid=2104391) charges
