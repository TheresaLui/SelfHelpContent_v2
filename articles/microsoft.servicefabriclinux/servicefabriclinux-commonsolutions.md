<properties
	pageTitle="advisory"
	description="advisory"
	service="microsoft.servicefabriclinux"
	resource="clusters"
	authors="ChiragPavecha, peterpogorski"
    ms.author="chiragpa, pepogors"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32589163,32589164,32589176,32589177,32589178,32589182,32589186,32589188,32589194,32589165,32589173,32589174,32589175,32589179,32589187,32589189,32589190,32589191,32589196,32589166,32589167,32589169,32589170,32589180,32589181,32589184,32589185,32589193,32589195,32598337,32589168,32589171,32589172,32589183,32589192"	
	resourceTags=""
	productPesIds="16147"
	cloudEnvironments="public"
	articleId="dff903db-a3a3-4260-90ad-b3480e608892"
/>

# Service Fabric Linux Common Solutions

## Active Known Issue with Service Fabric Linux Clusters 
A recent update introduced an issue for Service Fabric Linux clusters where Ubuntu based Service Fabric nodes will be unable to do core management operations unless the dependent package is downgraded to the previous version (2.3.4-4). 

**Impacted Customers:** Impact is limited to any new Azure based Service Fabric clusters, any new nodes added to an existing cluster, or any nodes which have the upgraded package version (this is applicable if you have manually requested a reimage of any VM(s) in your scale sets). If you are impacted by this issue you will see the Image Store Service is failing.

Existing clusters that have not been scaled up or do not have nodes that have been reimaged, should not be affected. 

## **Recommended Steps**
A script is available to help mitigate the issue. This needs to be applied as a Custom Script Extension to your ARM (Azure Resource Manager) template.

For detailed mitigation steps and support resources please see this [post](https://blogs.msdn.microsoft.com/azureservicefabric/2019/02/07/known-issue-for-service-fabric-linux-clusters/). 

## **Recommended Documents**

* [Patch Linux OS of your Service Fabric Cluster](https://docs.microsoft.com/azure/service-fabric/service-fabric-patch-orchestration-application-linux)<br>
* [Tutorial: Create container images on a Linux Service Fabric cluster](https://docs.microsoft.com/azure/service-fabric/service-fabric-tutorial-create-container-images)<br>
* [How to prepare development environment for Service Fabric Linux clusters](https://docs.microsoft.com/azure/service-fabric/service-fabric-get-started-linux)<br>
* [Troubleshooting guides on Certificate Configuration](https://github.com/Azure/Service-Fabric-Troubleshooting-Guides/blob/master/Security/README.md#certificate-configuration)<br>
* [Service Fabric Common Networking Scenarios](https://blogs.msdn.microsoft.com/kwill/2016/10/05/azure-service-fabric-common-networking-scenarios/)<br>
* [Certificates and Security on Linux Clusters](https://docs.microsoft.com/azure/service-fabric/service-fabric-configure-certificates-linux)
