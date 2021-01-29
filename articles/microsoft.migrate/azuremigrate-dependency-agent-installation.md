<properties 
    pageTitle="Installation issues with dependency agents"
    description="Issues and guidance regarding installation of Dependency Agents in Azure Migrate"
    service="microsoft.migrate"
    resource="migrateprojects"
    authors="An-mol"
    ms.author="anvar"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32675753"
    resourceTags=""
    productPesIds="16348"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="23107b51-5825-4eba-83ec-d29f6fb21ffc"
    ownershipId="Compute_AzureMigrate"
/>

# Installation of Dependency Agents

## **Recommended Steps**


### ***What are the supported operating systems for agent-based dependency analysis?***

Refer to the supported OS documentation [here](https://go.microsoft.com/fwlink/?linkid=2133723).

### ***I installed agents on my on-premises VMs, but the dependencies are not showing up. What should I do?***

Typically, the dependencies start showing up after 15-20 minutes of installing the agents. [Learn more about agent installation](https://docs.microsoft.com/azure/migrate/how-to-create-group-machine-dependencies#download-and-install-the-vm-agents).

### **I want to automate the installation of Microsoft Monitoring Agent (MMA) and dependency agent. How do I do that?**

You can use scripts to deploy the [dependency](https://docs.microsoft.com/azure/migrate/how-to-create-group-machine-dependencies#install-the-dependency-agent) and [MMA](https://docs.microsoft.com/azure/migrate/how-to-create-group-machine-dependencies#install-the-mma) agents. You can also leverage deployment tools such as System Center Configuration Manager (SCCM) and [Intigua](https://go.microsoft.com/fwlink/?linkid=2104196) to deploy the agents. The MMA agent can also be installed using this [script](https://go.microsoft.com/fwlink/?linkid=2104394).

### **Do I need to install Service Map agents if I have System Center Operations Manager set up already?**

For machines monitored by System Center Operations Manager 2012 R2 or later, there is no need to install the MMA agent. Service Map has an integration with SCOM that leverages the SCOM MMA to gather the necessary dependency data. You can enable the integration using the guidance [here](https://docs.microsoft.com/azure/azure-monitor/insights/service-map-scom#prerequisites). Note that the dependency agent will still need to be installed on these machines.

### **Is Agent-based dependency analysis available in Azure Government?**

Agent-based dependency analysis is not available in Azure Government. You can use agentless dependency analysis. Comparison [here](https://docs.microsoft.com/azure/migrate/concepts-dependency-visualization#compare-agentless-and-agent-based).
