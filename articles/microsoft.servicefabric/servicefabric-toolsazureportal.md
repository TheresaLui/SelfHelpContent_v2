<properties
	pageTitle="tools/azure portal"
	description="tools/azure portal"
	service="microsoft.servicefabric"
	resource="clusters"
	authors="cts-shrahman"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32518067"
	resourceTags=""
	productPesIds="15842"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="a810d1d5-cbbf-4938-9387-14fde6384bb4"
	ownershipId="Compute_ServiceFabric"
/>

# tools/azure portal

## **Recommended steps**
If your cluster is not starting or nodes are not displaying, try one or more of the following methods.

1. Review [Audit logs](data-blade:Microsoft_Azure_Insights.AzureDiagnosticsBladeWithParameter) to check for ARM deployment or resource allocation failures.
2. Review Network Settings to make sure NSG settings allow incoming traffic to port 19080 [Resource Group -> Virtual Network -> Subnets -> Security Group].
3. [RDP](https://azure.microsoft.com/documentation/articles/service-fabric-cluster-nodetypes/#remote-connect-to-a-vm-scale-set-instance-or-a-cluster-node) to one of the nodes and check the Application event logs and Microsoft-Service-Fabric Admin event logs for errors.  You may see several transient Warning entries in the SFAdmin logs which can be ignored. You will be looking for Error entries with descriptions related to cluster setup failures. 

