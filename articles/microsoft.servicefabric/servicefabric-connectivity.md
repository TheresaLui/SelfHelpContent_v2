<properties
	pageTitle="application/connectivity"
	description="application/connectivity"
	service="microsoft.servicefabric"
	resource="clusters"
	authors="cts-shrahman"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32449684"
	resourceTags=""
	productPesIds="15842"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="c698e9bf-96fc-4ac3-91a0-36d5d44b51ca"
	ownershipId="Compute_ServiceFabric"
/>

# application/connectivity

## **Recommended steps**

Common Failures and Troubleshooting Steps for an Application or Service:

1.	Check Service Fabric Explorer for information about the failure. See "I am seeing System.XXX Errors in Service Fabric Explorer" section and determine which node is failing.
2.	Check Application Event logs or ETW trace logs for exceptions being thrown.
3.	Make sure your async methods (OpenAsync, CloseAsync, RunAsync) correctly handle the CancellationToken since this is how Service Fabric triggers a replica to close.
4.	Make sure all application dependencies are included within your application package.
5.	Common failures are exceptions in entry point methods - RunAsync, OnActivateAsync, CreateServiceReplicaListeners, CreateServiceInstanceListeners, OnCloseAsync, OnOpenAsync
6.	Attach a debugger to your service.


<br>Connection failures to applications deployed in a cluster:

1. Verify that the Load Balancing Rules are mapping the exposed public port to the expected internal port and back end address pool [See Resource Group -> Load Balancer[LB-xxx] -> Load Balancing rules].
2. Verify that the ServiceManifest.xml has an Endpoint defined with the correct protocol and port mapping. See [Specify resources in a service manifest](https://azure.microsoft.com/documentation/articles/service-fabric-service-manifest-resources/).
3. Check for potential Network Security Group rules that could block traffic Network Settings [Resource Group -> Virtual Network -> Subnets -> Security Group].
4. Make sure the application is configured to listen on the correct port. Typically this is done in the CreateServiceInstanceListeners method by calling CodePackageActivationContext.GetEndpoint to get the endpoint configured in the service manifest.
5. For HTTP endpoints, RDP to one of the nodes running the application and from a command prompt execute:
       netsh http show servicestate view=requestq : This will show the process IDs and registered URLs for all services registered with http.sys.
6. RDP to one of the nodes running the application and use a network tracing tool (Netmon, Message Analyzer, Wireshark, etc) to watch for incoming traffic.  This will help determine if traffic is reaching the cluster or if the issue is somewhere between the client and the Azure load balancer.
7. Test from a different client to eliminate client side network issues, particularly if the client is in a corporate network environment where certain ports or traffic may be blocked.  Ideally test from another Azure VM in order to eliminate any possible networking issues outside of Azure.

## **Recommended documents**
1. [Monitor and diagnose services in a local machine development setup](https://azure.microsoft.com/documentation/articles/service-fabric-diagnostics-how-to-monitor-and-diagnose-services-locally/) for how to configure ETW traces in your application
2. [Debug your Service Fabric application by using Visual Studio](https://azure.microsoft.com/documentation/articles/service-fabric-debugging-your-application/) for how to use Visual Studio to debug and view ETW traces for a remote Service Fabric app
3. [Troubleshoot common issues](https://azure.microsoft.com/documentation/articles/service-fabric-diagnostics-troubleshoot-common-scenarios/)<br>
