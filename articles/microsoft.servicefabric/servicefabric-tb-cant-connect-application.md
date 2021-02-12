<properties 
	pageTitle="Connection failures to applications deployed in a cluster " 
	description="Connection failures to applications deployed in a cluster " 
	service="microsoft.servicefabric"
	resource="clusters"
	authors="pkcsf"
	displayOrder="9"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="servicefabric"
	productPesIds=""
	cloudEnvironments="public,BlackForest,Fairfax, usnat, ussec"	 
	articleId="4fe681ed-9d5e-4450-a664-36f2dbcb542d"
	ownershipId="Compute_ServiceFabric"
/>
 
# Connection failures to applications deployed in a cluster 

## **Recommended steps**

1. Verify that the Load Balancing Rules are mapping the exposed public port to the expected internal port and back end address pool [See Resource Group -> Load Balancer[LB-xxx] -> Load Balancing rules].
2. Verify that the ServiceManifest.xml has an Endpoint defined with the correct protocol and port mapping. See [Specify resources in a service manifest](https://azure.microsoft.com/documentation/articles/service-fabric-service-manifest-resources/).
3. Check for potential Network Security Group rules that could block traffic Network Settings [Resource Group -> Virtual Network -> Subnets -> Security Group].
4. Make sure the application is configured to listen on the correct port. Typically this is done in the CreateServiceInstanceListeners method by calling CodePackageActivationContext.GetEndpoint to get the endpoint configured in the service manifest.
5. For HTTP endpoints, RDP to one of the nodes running the application and from a command prompt execute:
       netsh http show servicestate view=requestq : This will show the process IDs and registered URLs for all services registered with http.sys.
6. RDP to one of the nodes running the application and use a network tracing tool (Netmon, Message Analyzer, Wireshark, etc) to watch for incoming traffic.  This will help determine if traffic is reaching the cluster or if the issue is somewhere between the client and the Azure load balancer.
7. Test from a different client to eliminate client side network issues, particularly if the client is in a corporate network environment where certain ports or traffic may be blocked.  Ideally test from another Azure VM in order to eliminate any possible networking issues outside of Azure.
