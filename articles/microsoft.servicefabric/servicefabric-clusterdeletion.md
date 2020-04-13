<properties
	pageTitle="cluster/cluster deletion"
	description="cluster/cluster deletion"
	service="microsoft.servicefabric"
	resource="clusters"
	authors="cts-shrahman"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32518063"
	resourceTags=""
	productPesIds="15842"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="00dc5f1a-43b2-4f68-a166-05fde3d38def"
	ownershipId="Compute_ServiceFabric"
/>

# cluster/cluster deletion

## **Recommended steps**
If your cluster is not starting or nodes are not displaying, try one or more of the following methods.

1. Review [Audit logs](data-blade:Microsoft_Azure_Insights.AzureDiagnosticsBladeWithParameter) to check for ARM deployment or resource allocation failures.
2. Review Network Settings to make sure NSG settings allow incoming traffic to port 19080 [Resource Group -> Virtual Network -> Subnets -> Security Group].
3. [RDP](https://azure.microsoft.com/documentation/articles/service-fabric-cluster-nodetypes/#remote-connect-to-a-vm-scale-set-instance-or-a-cluster-node) to one of the nodes and check the Application event logs and Microsoft-Service-Fabric Admin event logs for errors.  You may see several transient Warning entries in the SFAdmin logs which can be ignored. You will be looking for Error entries with descriptions related to cluster setup failures. 

