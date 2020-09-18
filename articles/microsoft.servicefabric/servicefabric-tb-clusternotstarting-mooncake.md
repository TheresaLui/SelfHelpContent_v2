<properties
    pageTitle="My cluster is not starting or nodes are not displaying"
    description="My cluster is not starting or nodes are not displaying"
    service="microsoft.servicefabric"
    resource="clusters"
    authors="pkcsf"
    ms.author="pkc"
    displayOrder="2"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="servicefabric"
    productPesIds=""
    cloudEnvironments="MoonCake"
	articleId="3acf1daa-ac94-43f1-8317-1a26771e363e"
	ownershipId="Compute_ServiceFabric"
/>

# My cluster is not starting or nodes are not displaying

## **Recommended Steps**

1. Review [Audit logs](data-blade:Microsoft_Azure_Insights.AzureDiagnosticsBladeWithParameter) to check for ARM deployment or resource allocation failures
2. Review Network Settings to make sure NSG settings allow incoming traffic to port 19080. To do this, go to **Resource Group**, **Virtual Network**, **Subnets**, **Security Group**.
3. [RDP](https://docs.azure.cn/service-fabric/service-fabric-cluster-nodetypes/#remote-connect-to-a-vm-scale-set-instance-or-a-cluster-node) to one of the nodes and check the Application event logs and Microsoft-Service-Fabric Admin event logs for errors. You may see several transient **Warning** entries in the SFAdmin logs, which can be ignored. You will be looking for **Error** entries with descriptions related to cluster setup failures. See most commonly used to troubleshoot problems:

    * Event Logs
        * Service Fabric Event Logs
        * Application and System Event Logs
        * Azure Event Logs
    * Azure Guest Agent logs
    * Extension/Plugin Setup Logs and Status Blobs
    * Node configuration
    * Service Fabric Installation Logs
    * Windows Azure Diagnostics logs and cached data
