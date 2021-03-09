<properties 
    pageTitle="Diagnose and resolve issues with Azure Spark monitor" 
    description="Diagnose and resolve issues with Azure Spark monitor" 
    service="microsoft.databricks" 
    resource="workspaces" 
    authors="lahaddad" 
    ms.author="lahaddad" 
    displayOrder="15" 
    selfHelpType="generic" 
    supportTopicIds="32784347" 
    resourceTags="" 
    productPesIds="16432" 
    cloudEnvironments="public, fairfax, usnat, ussec" 
    articleId="3f8ca876-a96e-4a24-8e39-264476b6e30b" 
    ownershipId="AzureData_AzureDatabricks" 
/> 

# Diagnose and resolve issues with Azure Spark Monitor 

## **Recommended Steps** 

You must configure an outbound rule for the **AzureMonitor** service tag if you:
-	deployed the Azure Databricks workspace in your own virtual network, and
-	configured network security groups (NSG) to deny all outbound traffic not required by Azure Databricks
 

## **Recommended Documents** 

* [Azure Monitor Overview](https://docs.microsoft.com/azure/azure-monitor/overview) 
* [Monitoring Azure Databricks](https://docs.microsoft.com/azure/architecture/databricks-monitoring/): 

  * [Send Azure Databricks application logs to Azure Monitor](https://docs.microsoft.com/azure/architecture/databricks-monitoring/application-logs) 
  
  * [Use dashboards to visualize Azure Databricks metrics](https://docs.microsoft.com/azure/architecture/databricks-monitoring/dashboards) 
  
  * [Troubleshoot performance bottlenecks](https://docs.microsoft.com/azure/architecture/databricks-monitoring/performance-troubleshooting) 
  
