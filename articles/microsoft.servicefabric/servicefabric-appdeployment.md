<properties
	pageTitle="application/deployment"
	description="application/deployment"
	service="microsoft.servicefabric"
	resource="clusters"
	authors="cts-shrahman"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32449685"
	resourceTags=""
	productPesIds="15842"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="51480ada-4f2c-4cf9-b03e-0e94619d9457"
	ownershipId="Compute_ServiceFabric"
/>

# application/deployment

## **Recommended steps**
Errors deploying a service:

1. The majority of deployment failures are caused by exceptions when a service is starting. This could be a missing dependency or exception in the constructor, or an exception in one of the Service Fabric startup methods (RunAsync, OnActivateAsync, CreateServiceReplicaListeners, CreateServiceInstanceListeners). See the 'Common Failures and Troubleshooting Steps for Application/Service' section for how to troubleshoot.
2. Verify that your instance/replica count does not exceed the size of your cluster.

Common Failures and Troubleshooting Steps for an Application or Service:

1.	Check Service Fabric Explorer for information about the failure. See "I am seeing System.XXX Errors in Service Fabric Explorer" section and determine which node is failing.
2.	Check Application Event logs or ETW trace logs for exceptions being thrown.
3.	Make sure your async methods (OpenAsync, CloseAsync, RunAsync) correctly handle the CancellationToken since this is how Service Fabric triggers a replica to close.
4.	Make sure all application dependencies are included within your application package.
5.	Common failures are exceptions in entry point methods - RunAsync, OnActivateAsync, CreateServiceReplicaListeners, CreateServiceInstanceListeners, OnCloseAsync, OnOpenAsync
6.	Attach a debugger to your service.



## **Recommended documents**
1. [Monitor and diagnose services in a local machine development setup](https://azure.microsoft.com/documentation/articles/service-fabric-diagnostics-how-to-monitor-and-diagnose-services-locally/) for how to configure ETW traces in your application
2. [Debug your Service Fabric application by using Visual Studio](https://azure.microsoft.com/documentation/articles/service-fabric-debugging-your-application/) for how to use Visual Studio to debug and view ETW traces for a remote Service Fabric app
3. [Troubleshoot common issues](https://azure.microsoft.com/documentation/articles/service-fabric-diagnostics-troubleshoot-common-scenarios/)<br>
