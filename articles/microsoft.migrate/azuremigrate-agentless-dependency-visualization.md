<properties
  pagetitle="Dependency analysis (agentless &amp; agent-based)"
  service="microsoft.migrate"
  resource="migrateprojects"
  ms.author="vivikram"
  selfhelptype="Generic"
  supporttopicids="32675744"
  resourcetags=""
  productpesids="16348"
  cloudenvironments="public,fairfax,usnat,ussec,blackforest,mooncake"
  articleid="b9c6cb48-0995-4ac5-82f1-fa6582eddf77"
  ownershipid="Compute_AzureMigrate" />
# Dependency analysis (agentless & agent-based)

Most users are able to resolve issues with dependency analysis (agentless and agent-based) issues by using the steps below.

## **Recommended Steps**

### **Dependency analysis (agentless)**

### **I want access to use the agentless dependency analysis feature. How do I do that?**

Agentless dependency analysis is no longer in limited preview and is available for everyone to use on Azure Portal. There is no need to use any preview URL.

### **I see "Unknown process" in the exported CSV.**

Refer to the [troubleshooting documentation](https://docs.microsoft.com/azure/migrate/troubleshoot-assessment#dependencies-export-csv-shows-unknown-process).

### **I see empty values in the CSV for application, process, and server.**

The server name, application, and process fields are populated only for servers that have agentless dependency analysis enabled. It is on the backlog to show server name for all Azure Migrate discovered machines, and not just the ones enabled for dependency analysis. 

### **I want to run analysis on more than 1000 servers at a time.**

Dependency analysis can be run only on 1000 VMs at a time in one project. There is no way to make an exception. If you have more than 1000 VMs, you can sequence the analysis in batches of 1000 at a time.

### **Can I visualize the map and export dependencies for a VM on which I have stopped dependency data collection?**

Yes, you will be able to view the dependencies in a map and export the dependencies even after you stop the data collection. All data gathered in the 30 days can be reviewed.

### **I see a dependency map with 0 processes.**

Ensure that the [necessary prerequisites](https://docs.microsoft.com/azure/migrate/migrate-support-matrix-vmware#agentless-dependency-visualization) are met for agentless dependency analysis.

### **What are the privileges required to set up agentless dependency analysis?**

Review the [prerequisites for agentless dependency analysis](https://docs.microsoft.com/azure/migrate/migrate-support-matrix-vmware#agentless-dependency-visualization).

### **Dependency analysis (agent-based)**

### **I installed agents on my on-premises VMs, but the dependencies are not showing up.**

Typically, the dependencies start showing up after 15-20 minutes of installing the agents. Ensure tha the dependency agent is up and running. Ensure that the server operating system is [supported](https://go.microsoft.com/fwlink/?linkid=2133723). See [troubleshooting guidance](https://docs.microsoft.com/azure/azure-monitor/insights/service-map#post-installation-issues).

### **What are the supported operating systems for agent-based dependency analysis?**

See the [supported OS documentation](https://go.microsoft.com/fwlink/?linkid=2133723).

### **Is there a charge for using dependency visualization?**

The [Service Map solution](https://go.microsoft.com/fwlink/?linkid=2104198) will not incur any charges for the first 180 days from the day of associating the [Log Analytics](https://go.microsoft.com/fwlink/?linkid=2104198) workspace with Server Assessment. After 180 days, standard Log Analytics charges will apply.

The use of any solution other than Service Map within the linked OMS workspace will incur standard [Log Analytics](https://go.microsoft.com/fwlink/?linkid=2104391) charges.

## Workspace association and agent installation

### **I am not able to associate my Log Analytics workspace with the Azure Migrate project or use the region of my preference. How do I proceed?**

Azure Migrate currently supports creation or associations of OMS workspaces that are in East US, Southeast Asia, and West Europe regions. Even if the workspace is created outside of Azure Migrate in an unsupported region, it currently cannot be associated with an Azure Migrate project. 

### **Can I change the OMS workspace used by Server Assessment?**

No, you cannot change the OMS workspace after it has been configured.

### **I want to automate the installation of Microsoft Monitoring Agent (MMA) and the dependency agent. How do I do that?**

You can use scripts to deploy the [dependency](https://go.microsoft.com/fwlink/?linkid=2104389) and [MMA](https://go.microsoft.com/fwlink/?linkid=2104390) agents. You can also leverage deployment tools such as System Center Configuration Manager (SCCM) and [Intigua](https://go.microsoft.com/fwlink/?linkid=2104196) to deploy the agents. The MMA agent can also be installed using this [script](https://go.microsoft.com/fwlink/?linkid=2104394).

## Visualization and export

### **Is dependency visualization supported for groups with more than 10 VMs?**

You can visualize dependencies of groups with up to 10 VMs. However, you can use Azure Monitor logs to [query the dependency data](https://go.microsoft.com/fwlink/?linkid=2104393) in a tabular format for any number of VMs. If you are aiming only to visualize dependencies, we recommend you split the group into smaller groups and visualize dependencies.

### **Can I visualize dependencies for more than one-hour duration?**

No, Server Assessment lets you visualize dependencies for up to one hour. You can go back to any specific date in the last one month, but the duration for which you can visualize the dependencies is up to one hour. However, you can use Azure Monitor logs to [query the dependency data](https://go.microsoft.com/fwlink/?linkid=2104393) in a tabular format over a longer duration.

### **I want to retrieve connection port and data volume information using Service Map. How do I do that?**

Retrieve TCP connection port and data volume information by running Log Analytics queries. [Learn more](https://go.microsoft.com/fwlink/?linkid=2104393) about sample queries and how they can be run.

### **Can I export the dependency visualization report?**

You can retrieve dependency information by running Log Analytics queries. [Learn more](https://go.microsoft.com/fwlink/?linkid=2104393) about sample queries and how they can be run.

## Other issues

### **I want to configure Azure Migrate: Server Assessment to use an existing OMS workspace. How do I do that?**

When you configure your OMS workspace for the first time for an Azure Migrate: Server Assessment project, you can either create a new workspace or use an existing OMS workspace. [Learn more](https://go.microsoft.com/fwlink/?linkid=2104261) about how to configure an OMS workspace in Server Assessment.

### **Do I need to install Service Map agents if I have System Center Operations Manager set up already?**

For machines monitored by System Center Operations Manager 2012 R2 or later, there is no need to install the MMA agent. Service Map has an integration with SCOM that leverages the SCOM MMA to gather the necessary dependency data. You can enable the integration by using the [guidance](https://go.microsoft.com/fwlink/?linkid=2104197). Note that the dependency agent will still need to be installed on these machines.
