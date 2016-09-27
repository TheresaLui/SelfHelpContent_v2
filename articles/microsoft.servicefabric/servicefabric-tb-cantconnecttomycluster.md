<properties 
	pageTitle="I can't connect to my cluster" 
	description="I can't connect to my cluster" 
	service="microsoft.servicefabric"
	resource="servicefabric"
	authors="pkcsf"
	displayOrder="5"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="servicefabric"
	productPesIds=""
	cloudEnvironments="public"	 
/>
 
# I can't connect to my cluster

## **Connection failures using Service Fabric Explorer (SFX) or Powershell to the Management Endpoint**
Try to browse to the SFX https endpoint (URL found on the Azure management portal, typically https://{clustername}.{region}.cloudapp.azure.com:19080/Explorer)

1. If you get a connection failure it means https traffic cannot be made to port 19080.
   + Validate the connection failure by using telnet to try to reach the IP address and port 19080.
   + Make sure you are browsing to https and not http for the management endpoint.
   + Check for a Network Security Group that could block traffic
   + Make sure the cluster is running and nodes are visible in the management portal (see [My cluster is not starting or nodes are not displaying] (data-blade:servicefabric-tb-clusternotstarting.md)
   + Check for client side networking issues such as a Proxy server that might be blocking traffic
   
2. If you get a certificate related error it means you can connect to port 19080, but there may be a certificate problem
   + If you get a warning that the certificate is not trusted or the domain name does not match
     + You might be using a self-signed certificate which is not chained to a root CA.  You can either get a signed certificate from a certificate authority, or you can add your self-signed certificate to your trusted root store.
     + You might be using a certificate with a different subject name than the DNS name you are browsing to.  You can setup a DNS mapping (CNAME, A record, or local hosts file) to map your certificates subject name (for example, servicefabric.mycompany.com) to the Service Fabric management endpoint (for example, mycluster.westus.cloudapp.azure.com), and then try browsing to your custom domain name (https://servicefabric.mycompany.com:19080/Explorer)
     +	If you trust the server certificate that is presented, then you can just ignore the certificate warning in the browser and continue to the site.
   + When connecting to a cluster which is secured by a certificate you must present a certificate in order to authenticate your client.  To do this make sure the cluster security certificate is in your personal certificate store.  When browsing to the management endpoint your web browser should prompt you to select a client certificate, at which time you can choose the cluster cert from your certificate store.
   + If you are connecting with Powershell you need the cluster certificate in your personal certificate store, as above in (b), and you need to specify the client certificate in Powershell when connecting to the cluster.  See [Connect to a secure cluster](https://azure.microsoft.com/documentation/articles/service-fabric-connect-to-secure-cluster/)
 
## **Connection failures to applications deployed in a cluster**

1. Verify that the Load Balancing Rules are mapping the exposed public port to the expected internal port and back end address pool [Load Blancing Rules](data-blade:loadblancing rule)
2. Verify that the ServiceManifest.xml has an Endpoint defined with the correct protocol and port mapping.  See [Specify resources in a service manifest](https://azure.microsoft.com/documentation/articles/service-fabric-service-manifest-resources/)
3. Check for potential Network Security Group rules that could block traffic [Network Settings](data-blade:Microsoft_Azure_Network.EffectiveSecurityRulesBlade)
4. Make sure the application is configured to listen on the correct port. Typically this is done in the CreateServiceInstanceListeners method by calling CodePackageActivationContext.GetEndpoint to get the endpoint configured in the service manifest.
5. For HTTP endpoints, RDP to one of the nodes running the application and from a command prompt execute:
       netsh http show servicestate view=requestq : This will show the process IDs and registered URLs for all services registered with http.sys.
6. RDP to one of the nodes running the application and use a network tracing tool (Netmon, Message Analyzer, Wireshark, etc) to watch for incoming traffic.  This will help determine if traffic is reaching the cluster or if the issue is somewhere between the client and the Azure load balancer.
7. Test from a different client to eliminate client side network issues, particularly if the client is in a corporate network environment where certain ports or traffic may be blocked.  Ideally test from another Azure VM in order to eliminate any possible networking issues outside of Azure.
 
