<properties
	pageTitle="Azure Service Fabric"
	description="Issues related to service fabric deployment and usage with the task"
	infoBubbleText="Azure Pipelines issues related to service fabric deployment and usage with the task"
	service="microsoft.visualstudio"
	resource="account"
	authors="v-abiss"
	ms.author="v-abiss"
	articleId="AzureServiceFabric"
	supportTopicIds="32742302"
	diagnosticScenario=""
	selfHelpType="generic"
	resourceTags=""
	productPesIds="15543"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Azure_DevOps_Services"
/>

# Azure Pipeline issues during service fabric deployment and use

#### **Common Azure Pipeline issues during service fabric deployment and use**

* **Release pipeline fails due to an invalid client certificate used with the deployment**

   Ensure that your certificate is not expired. If it is expired, create a new one and update the release pipeline task with new client certificate. See [these instructions](https://docs.microsoft.com/azure/service-fabric/service-fabric-tutorial-deploy-app-with-cicd-vsts).
    
* **System.Fabric.FabricTransientException: Could not ping any of the provided Service Fabric gateway endpointswarning** while running two releases on the same machine

   Currently, [Service fabric tasks in Azure DevOps](https://docs.microsoft.com/azure/devops/pipelines/tasks/deploy/service-fabric-deploy?view=azure-devops) has a limitation for running multiple releases that target the same service connection. In such cases, when two releases run on the same machine, one of the tasks completes and the certificate in the machine cert store is cleaned. Therefore, the second release fails. If there are multiple service connections using same certificate, then the releases using those connections will also fail. We recommend using different agents (on different machines) for parallel service fabric tasks that target the same connection.
    
#### **Recommended Documents**

* [Tutorial: Deploy an application with CI/CD to a Service Fabric cluster](https://docs.microsoft.com/azure/service-fabric/service-fabric-tutorial-deploy-app-with-cicd-vsts)
* [Service Fabric Application Deployment task](https://docs.microsoft.com/azure/devops/pipelines/tasks/deploy/service-fabric-deploy?view=azure-devops)
* [Azure Service Fabric application and cluster best practices](https://docs.microsoft.com/azure/service-fabric/service-fabric-best-practices-overview)
* [Capacity planning and scaling for Azure Service Fabric](https://docs.microsoft.com/azure/service-fabric/service-fabric-best-practices-capacity-scaling)
