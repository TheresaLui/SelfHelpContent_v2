<properties 
    pageTitle="Connection failures to applications deployed in a cluster"
    description="Connection failures to applications deployed in a cluster"
    service="microsoft.servicefabric"
    resource="clusters"
    authors="pkcsf"
    ms.author="pkc"
    displayOrder="9"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="servicefabric"
    productPesIds=""
    cloudEnvironments="MoonCake"
	articleId="03d4c6ed-690c-48b3-ad68-2a8c7c4e4e8b"
	ownershipId="Compute_ServiceFabric"
/>

# Connection failures to applications deployed in a cluster

## **Recommended Steps**

1. Verify that the Load Balancing Rules are mapping the exposed public port to the expected internal port and back end address pool. To do this, click on **Resource Group**, then **Load Balancer[LB-xxx]**, and finally **Load Balancing Rules**.
2. Verify that the `ServiceManifest.xml` has an [endpoint defined with the correct protocol and port mapping](https://docs.azure.cn/service-fabric/service-fabric-service-manifest-resources/)
3. Check for potential Network Security Group rules that could block traffic Network Settings. To do this, click on **Resource Group**, **Virtual Network**, **Subnets**, **Security Group**. 
4. Make sure the application is configured to listen on the correct port. Typically, this is done in the `CreateServiceInstanceListeners` method by calling `CodePackageActivationContext.GetEndpoint` to get the endpoint configured in the service manifest.
5. For HTTP endpoints, RDP to one of the nodes running the application and from a command prompt execute `netsh http show servicestate view=requestq`. This will show the process IDs and registered URLs for all services registered with http.sys.
6. RDP to one of the nodes running the application and use a network tracing tool (Netmon, Message Analyzer, Wireshark, etc.) to watch for incoming traffic  This will help determine if traffic is reaching the cluster or if the issue is somewhere between the client and the Azure load balancer.
7. Test from a different client to eliminate client-side network issues, particularly if the client is in a corporate network environment where certain ports or traffic may be blocked. Ideally, test from another Azure VM to eliminate any possible networking issues outside of Azure.
