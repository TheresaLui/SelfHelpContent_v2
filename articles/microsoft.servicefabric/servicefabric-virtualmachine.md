<properties
	pageTitle="cluster/virtual machines"
	description="cluster/virtual machines"
	service="microsoft.servicefabric"
	resource="clusters"
	authors="cts-shrahman"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32449699"
	resourceTags=""
	productPesIds="15842"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="a92a0250-787f-40d2-a458-00c2eb0d4f7b"
	ownershipId="Compute_ServiceFabric"
/>

# cluster/virtual machines

## **Recommended steps**
If your cluster is not starting or nodes are not displaying, try one or more of the following methods.

1. Review [Audit logs](data-blade:Microsoft_Azure_Insights.AzureDiagnosticsBladeWithParameter) to check for ARM deployment or resource allocation failures.
2. Review Network Settings to make sure NSG settings allow incoming traffic to port 19080 [Resource Group -> Virtual Network -> Subnets -> Security Group].
3. [RDP](https://azure.microsoft.com/documentation/articles/service-fabric-cluster-nodetypes/#remote-connect-to-a-vm-scale-set-instance-or-a-cluster-node) to one of the nodes and check the Application event logs and Microsoft-Service-Fabric Admin event logs for errors.  You may see several transient Warning entries in the SFAdmin logs which can be ignored. You will be looking for Error entries with descriptions related to cluster setup failures. 

