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
    cloudEnvironments="public, Fairfax"
    articleId="23107b51-5825-4eba-83ec-d29f6fb21ffc"
	ownershipId="Compute_AzureMigrate"
/>

# Installation of Dependency Agents

## **Recommended Steps**

### ***I installed agents on my on-premises VMs, but the dependencies are not showing up. What should I do?***

Typically, the dependencies start showing up after 15-20 minutes of installing the agents. [Learn more about agent installation](https://aka.ms/migrate/dependencies/agent).

### **I want to automate the installation of Microsoft Monitoring Agent (MMA) and dependency agent. How do I do that?**

You can use scripts to deploy the [dependency](https://aka.ms/migrate/dependencies/dependencyagent) and [MMA](https://aka.ms/migrate/dependencies/mmaagent) agents. You can also leverage deployment tools such as System Center Configuration Manager (SCCM) and [Intigua](https://aka.ms/migrate/dependency_intigua) to deploy the agents. The MMA agent can also be installed using this [script](https://aka.ms/migrate/dependency_scriptinstaller).

### **Do I need to install Service Map agents if I have System Center Operations Manager set up already?**

For machines monitored by System Center Operations Manager 2012 R2 or later, there is no need to install the MMA agent. Service Map has an integration with SCOM that leverages the SCOM MMA to gather the necessary dependency data. You can enable the integration using the guidance [here](https://aka.ms/migrate/selfhelp/agentinstall_scomprereq). Note that the dependency agent will still need to be installed on these machines.
