<properties 
    pageTitle="Agentless Dependency Visualization"
    description="Issues and guidance regarding Agentless Dependency analysis feature in Azure Migrate: Server Assessment"
    service="microsoft.migrate"
    resource="migrateprojects"
    authors="rashi-ms"
    ms.author="rajosh"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32691004"
    resourceTags=""
    productPesIds="16348"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="b9c6cb48-0995-4ac5-82f1-fa6582eddf77"
	ownershipId="Compute_AzureMigrate"
/>

# Agentless dependency analysis

## **Recommended Steps**

### **I want access to use the Agentless dependency analysis feature. How do I do that?**

Agentless dependency analysis is available in a limited preview currently, and only for VMware VMs. Please submit a request at [this link](https://forms.office.com/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR35qjpJOBF1MmO4OLvbG-VVUM1UzOVAzVTY2MlM1NE5WMlJXSUhCTkRMOC4u) for access to the preview. Note you can access the preview only when you receive an invitation email. 

### **I have not received an email invitation even after submitting the request for the preview.**

Expect a delay of 2 weeks to get the invitation email. If you require urgent access, please go ahead and file the case to expedite access providing information on the business urgency. 


### **I see "Unknown process" in the exported CSV**

* Refer to the troubleshooting [documentation](https://docs.microsoft.com/azure/migrate/troubleshoot-assessment#dependencies-export-csv-shows-unknown-process)

### **I see empty values in the CSV for application, process and server**

The server name, application and process fields are populated only for servers that have agentless dependency analysis enabled. It is on the backlog to show server name for all Azure Migrate discovered machines, and not just the ones enabled for dependency analysis. 

### **I want to run analysis on more than 100 servers at a time**

Dependency analysis can be run only on a 100 VMs at a time in one project. There is no way to make an exception. Higher concurrent scale will be supported soon.

### **Can I visualize the map and export dependencies for a VM on which I have stopped dependency data collection**

Yes, you will be able to view the dependencies in a map and export the dependencies even after you stop the data collection. All data gathered in the 30 days can be reviewed.

### **My subscription is whitelisted but I still don't see the Add/Remove server tab to enable the dependency. How do I proceed?**

You are not enabled for the preview until you get an email invitation from the product group. If you have received the email invitation, please ensure that you use the URL provided in the email. Agentless dependency is still in private preview, and the feature is not accessible using the standard "portal.azure.com" URL.

### **I see a dependency map with 0 processes**

Ensure the [necessary prerequisites](https://docs.microsoft.com/azure/migrate/migrate-support-matrix-vmware#agentless-dependency-visualization) are met for agentless dependency analysis.

### **What are the privileges required to set up agentless dependency analysis**

Review the necessary prerequisites for agentless dependency analysis [here](https://docs.microsoft.com/azure/migrate/migrate-support-matrix-vmware#agentless-dependency-visualization).

### **Have I been enabled for the preview?**

If you are enabled, you would have received an invitation via email. 

