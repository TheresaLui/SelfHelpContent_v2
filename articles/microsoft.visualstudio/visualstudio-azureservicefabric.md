<properties
  pagetitle="Azure Pipeline issues during service fabric deployment and use"
  description="Issues related to service fabric deployment and usage with the task"
  service="microsoft.visualstudio"
  resource="account"
  ms.author="v-abiss,cathmill"
  selfhelptype="Generic"
  supporttopicids="32742302"
  resourcetags=""
  productpesids="15543"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="azureservicefabric"
  ownershipid="Azure_DevOps_Services" />
# Azure Pipeline issues during service fabric deployment and use

## Common Azure Pipeline issues during service fabric deployment and use

Resolve most common Azure Pipeline issues with the following solutions.

* Release pipeline fails due to an invalid client certificate used with the deployment

   Ensure that your certificate is not expired. If it is expired, create a new one and update the release pipeline task with new client certificate. See [these instructions](https://docs.microsoft.com/azure/service-fabric/service-fabric-tutorial-deploy-app-with-cicd-vsts).
    
* "System.Fabric.FabricTransientException: Could not ping any of the provided Service Fabric gateway endpoints warning" while running two releases on the same machine

   Currently, [Service fabric tasks in Azure DevOps](https://docs.microsoft.com/azure/devops/pipelines/tasks/deploy/service-fabric-deploy?view=azure-devops) have a limitation for running multiple releases that target the same service connection. In such cases, when two releases run on the same machine, one of the tasks completes and the certificate in the machine cert store is cleaned. However, the second release fails. If there are multiple service connections using same certificate, releases using those connections will also fail. We recommend using different agents (on different machines) for parallel service fabric tasks that target the same connection.
    
## **Recommended Documents**

* [Tutorial: Deploy an application with CI/CD to a Service Fabric cluster](https://docs.microsoft.com/azure/service-fabric/service-fabric-tutorial-deploy-app-with-cicd-vsts)
* [Service Fabric Application Deployment task](https://docs.microsoft.com/azure/devops/pipelines/tasks/deploy/service-fabric-deploy?view=azure-devops)
* [Azure Service Fabric application and cluster best practices](https://docs.microsoft.com/azure/service-fabric/service-fabric-best-practices-overview)
* [Capacity planning and scaling for Azure Service Fabric](https://docs.microsoft.com/azure/service-fabric/service-fabric-best-practices-capacity-scaling)
* For service-impacting issues, see [Azure DevOps Services Status](https://status.dev.azure.com/)
* Want a quicker answer? For quick answers to common questions and issues, try the [Azure DevOps Virtual Agent](https://azuredevopsvirtualagent.azurewebsites.net/)
