<properties 
	pageTitle="My cluster is not starting or nodes are not displaying" 
	description="My cluster is not starting or nodes are not displaying" 
	service="microsoft.servicefabric"
	resource="servicefabric"
	authors="pkcsf"
	displayOrder="2"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="servicefabric"
	productPesIds=""
	cloudEnvironments="public"	 
/>
    
# My cluster is not starting or nodes are not displaying

## **Recommended steps**
1. Review [Audit logs](data-blade:Microsoft_Azure_Insights.AzureDiagnosticsBladeWithParameter) to check for ARM deployment or resource allocation failures
2. Review [Network Settings](data-blade:Microsoft_Azure_Network.EffectiveSecurityRulesBlade) to make sure NSG settings allow incoming traffic to port 19080.
3. [RDP](https://azure.microsoft.com/documentation/articles/service-fabric-cluster-nodetypes/#remote-connect-to-a-vm-scale-set-instance-or-a-cluster-node) to one of the nodes and check the Application event logs and Microsoft-Service-Fabric Admin event logs for errors.  You may see several transient Warning entries in the SFAdmin logs which can be ignored. You will be looking for Error entries with descriptions related to cluster setup failures.  See [Common log files](data-bade:servicefabric.Common log files for Service Fabric nodes) for more information on the log files.
