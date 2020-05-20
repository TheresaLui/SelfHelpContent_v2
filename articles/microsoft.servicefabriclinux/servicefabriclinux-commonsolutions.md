<properties
	pageTitle="advisory"
	description="advisory"
	service="microsoft.servicefabriclinux"
	resource="clusters"
	authors="ChiragPavecha"
  ms.author="chiragpa"
	displayOrder=""
	selfHelpType="generic"
supportTopicIds="32589163,32589164,32589176,32589177,32589178,32589182,32589186,32589188,32589194,32589165,32589173,32589174,32589175,32589179,32589187,32589189,32589190,32589191,32589196,32589166,32589167,32589169,32589170,32589180,32589181,32589184,32589185,32589193,32589195,32598337,32589168,32589171,32589172,32589183,32589192"	
	resourceTags=""
	productPesIds="16147"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="dff903db-a3a3-4260-90ad-b3480e608892"
	ownershipId="Compute_ServiceFabric"
/>

# Service Fabric Linux Common Solutions

## Resolution to previous ImageBuilder process issue for Service Fabric Linux clusters

As of Service Fabric runtime version 6.4.644 for Linux clusters, a previous issue with the ImageBuilder process has been resolved. This issue had required the addition of a custom script extension to the Azure Resource Manager template. This custom script extension can now be removed for clusters running Service Fabric runtime version 6.4.6444+. Please see this [post](https://blogs.msdn.microsoft.com/azureservicefabric/2019/04/17/resolution-to-previous-imagebuilder-process-issue-for-service-fabric-linux-clusters/) for more information.

## **Recommended Documents**

* [Patch Linux OS of your Service Fabric Cluster](https://docs.microsoft.com/azure/service-fabric/service-fabric-patch-orchestration-application-linux)<br>
* [Tutorial: Create container images on a Linux Service Fabric cluster](https://docs.microsoft.com/azure/service-fabric/service-fabric-tutorial-create-container-images)<br>
* [How to prepare development environment for Service Fabric Linux clusters](https://docs.microsoft.com/azure/service-fabric/service-fabric-get-started-linux)<br>
* [Troubleshooting guides on Certificate Configuration](https://github.com/Azure/Service-Fabric-Troubleshooting-Guides/blob/master/Security/README.md#certificate-configuration)<br>
* [Service Fabric Common Networking Scenarios](https://blogs.msdn.microsoft.com/kwill/2016/10/05/azure-service-fabric-common-networking-scenarios/)<br>
* [Certificates and Security on Linux Clusters](https://docs.microsoft.com/azure/service-fabric/service-fabric-configure-certificates-linux)
