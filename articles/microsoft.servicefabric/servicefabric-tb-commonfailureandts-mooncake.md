<properties 
    pageTitle="Common Failures and Troubleshooting Steps for Application/Service" 
    description="Common Failures and Troubleshooting Steps for Application/Service" 
    service="microsoft.ServiceFabric"
    resource="clusters"
    authors="pkcsf"
    ms.author="pkc"
    displayOrder="4"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="servicefabric"
    productPesIds=""
    cloudEnvironments="MoonCake"
	articleId="c31f26e0-d22e-4cc9-a02f-0401370def63"
	ownershipId="Compute_ServiceFabric"
/>

# Common Failures and Troubleshooting Steps for Application/Service

## **Recommended Steps**

1. Check Service Fabric Explorer for information about the failure. See "I am seeing System.XXX Errors in Service Fabric Explorer" section and determine which node is failing.
2. Check Application Event logs or ETW trace logs for exceptions being thrown
3. Make sure your async methods (OpenAsync, CloseAsync, RunAsync) correctly handle the CancellationToken since this is how Service Fabric triggers a replica to close
4. Make sure all application dependencies are included within your application package
5. Common failures are exceptions in entry point methods - RunAsync, OnActivateAsync, CreateServiceReplicaListeners, CreateServiceInstanceListeners, OnCloseAsync, OnOpenAsync
6. Attach a debugger to your service

## **Recommended Documents**

1. [Monitor and diagnose services in a local machine development setup](https://docs.azure.cn/service-fabric/service-fabric-diagnostics-how-to-monitor-and-diagnose-services-locally/) for how to configure ETW traces in your application
2. [Debug your Service Fabric application by using Visual Studio](https://docs.azure.cn/service-fabric/service-fabric-debugging-your-application/) for how to use Visual Studio to debug and view ETW traces for a remote Service Fabric app
