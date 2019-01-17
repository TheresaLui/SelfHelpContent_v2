<properties
    pageTitle="SeedNodeDeleted"
    description="Detected one or more missing seed nodes"
    infoBubbleText="Detected one or more missing seed nodes. See details on the right."
    service="microsoft.servicefabric"
    resource="clusters"
    authors="a-santamaria"
    displayOrder=""
    articleId="SFSeedNodeInsightArticle"
    diagnosticScenario="SFSeedNodeInsight"
    selfHelpType="rca"
    supportTopicIds="32608928,32608936,32608960,32608935"
    resourceTags=""
    productPesIds="15842"
    cloudEnvironments="public"
/>

# Detected one or more missing seed nodes

<!--issueDescription-->
We have detected one or more missing **seed nodes** in your Service Fabric cluster.  
<!--/issueDescription-->

## **Recommended steps**
[Missing seed nodes with automated script](https://github.com/Azure/Service-Fabric-Troubleshooting-Guides/blob/master/Cluster/How%20to%20fix%20missing%20seednodes%20with%20Automated%20script.md)

## **What are seed nodes?**
Nodes with the "Is Seed Node = true" designation are the nodes in the Primary NodeType configured to host replicas of the system services (fabric:/system/...), based on the Reliability tier the cluster is configured for.  Service Fabric requires a quorum of seed nodes to be available and healthy to ensure cluster reliability.  We strongly recommend you take steps to repair/replace this missing seed node to prevent cluster instability or blocked upgrades.

See [Reliability characteristics of the cluster](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-capacity#the-reliability-characteristics-of-the-cluster) for more information about the number of seed nodes required for each reliability tier.

## **Common causes**
This issue commonly happens in one of the following scenarios:

1. [Scaling down the primary nodetype](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-scale-up-down) (VMMS) to less than the minimum number required based on the cluster [Reliability level](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-capacity#the-reliability-characteristics-of-the-cluster)
2. Configuring Auto-scale on clusters with [Bronze durability](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-capacity#the-durability-characteristics-of-the-cluster). Silver or Gold durability is required if you want to use Auto-scale with a Service Fabric cluster.
3. Improperly removing VM's from the primary nodetype without calling [Disable-ServiceFabricNode](https://docs.microsoft.com/powershell/module/servicefabric/disable-servicefabricnode?view=azureservicefabricps) with -Intent ‘**RemoveNode**’ to disable the node you’re going to remove and replace it with a new seed node.  This command is what tells the Service Fabric Resource Provider to elect a new seed node.  **Note:** There needs to be at least one 'non-seed node' in the VMMS available to be promoted to the new seed node.

## **Recommended documents**

* [Auto-scale with Service Fabric clusters](https://github.com/Azure/Service-Fabric-Troubleshooting-Guides/blob/master/Cluster/Common%20issues%20customers%20experience%20when%20using%20Auto-scale%20with%20Service%20Fabric%20clusters.md)
* [How to Fix one missing seed node](https://github.com/Azure/Service-Fabric-Troubleshooting-Guides/blob/master/Cluster/How%20to%20Fix%20one%20missing%20seed%20node.md)
* [How to Fix two missing seed node](https://github.com/Azure/Service-Fabric-Troubleshooting-Guides/blob/master/Cluster/How%20to%20Fix%20two%20missing%20seed%20node.md)
* [Service fabric cluster programmatic scaling](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-programmatic-scaling)

