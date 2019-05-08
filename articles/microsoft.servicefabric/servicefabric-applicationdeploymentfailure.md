<properties
	pageTitle="application/deploymentfailures"
	description="application/deploymentfailures"
	service="microsoft.servicefabric"
	resource="clusters"
	authors="chiragpa"
    ms.author="chiragpa"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32608937"
	resourceTags=""
	productPesIds="15842"
	cloudEnvironments="public"
	articleId="a179d458-e2a6-4e16-bdb8-5104b3d3d166"
/>

# application/deploymentfailures

## Active Known Issue with Service Fabric Linux Clusters 
A recent update introduced an issue for Service Fabric Linux clusters where Ubuntu based Service Fabric nodes will be unable to do core management operations unless the dependent package is downgraded to the previous version (2.3.4-4). 

**Impacted Customers:** This will affect all customers running Azure Service Fabric Linux clusters.

## **Recommended Steps**
A script is available to help mitigate the issue. This needs to be applied as a Custom Script Extension to your ARM (Azure Resource Manager) template.

For detailed mitigation steps and support resources please see this [post](https://blogs.msdn.microsoft.com/azureservicefabric/2019/02/07/known-issue-for-service-fabric-linux-clusters/). 

## **Recommended Documents**

* [Monitor and diagnose your application using ETW traces ](https://azure.microsoft.com/documentation/articles/service-fabric-diagnostics-how-to-monitor-and-diagnose-services-locally)<br>
* [Debug your Service Fabric application by using Visual Studio](https://azure.microsoft.com/documentation/articles/service-fabric-debugging-your-application/)<br>
* [Troubleshoot common issues](https://azure.microsoft.com/documentation/articles/service-fabric-diagnostics-troubleshoot-common-scenarios/)<br>
* [Continuous Deployment of Service Fabric Apps using VSTS (or TFS)](https://colinsalmcorner.com/post/continuous-deployment-of-service-fabric-apps-using-vsts-or-tfs)<br>
* [Tutorial: Build and Deploy a .Net App](https://docs.microsoft.com/azure/service-fabric/service-fabric-tutorial-create-dotnet-app)<br>
* [Tutorial: Build and Deploy a Java App](https://docs.microsoft.com/azure/service-fabric/service-fabric-tutorial-create-java-app)<br>
