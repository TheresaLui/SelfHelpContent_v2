<properties 
	pageTitle="Connection failures using Service Fabric Explorer (SFX) or PowerShell to the Management Endpoint " 
	description="Connection failures using Service Fabric Explorer (SFX) or PowerShell to the Management Endpoint " 
	service="microsoft.servicefabric"
	resource="clusters"
	authors="pkcsf"
	displayOrder="8"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="servicefabric"
	productPesIds=""
	cloudEnvironments="public,BlackForest,Fairfax, usnat, ussec"	 
	articleId="3488103d-e0b8-4585-84e8-4c58663eeb5c"
	ownershipId="Compute_ServiceFabric"
/>
 
# Connection failures using Service Fabric Explorer (SFX) or PowerShell to the Management Endpoint 

## **Recommended steps**

Try to browse to the SFX https endpoint (URL found on the Azure management portal, typically https://{clustername}.{region}.cloudapp.azure.com:19080/Explorer).  

1. If you get a connection failure it means https traffic cannot be made to port 19080.
  + Validate the connection failure by using telnet to try to reach the IP address and port 19080.
  +	Make sure you are browsing to https and not http for the management endpoint.
  +	Check for a Network Security Group that could block traffic.
  +	Make sure the cluster is running and nodes are visible in the management portal (see "My cluster is not starting or nodes are not displaying" section). 
  +	Check for client side networking issues such as a Proxy server that might be blocking traffic.

2.	If you get a certificate related error it means you can connect to port 19080, but there may be a certificate problem
  + You might be using a self-signed certificate which is not chained to a root CA.  You can either get a signed certificate from a certificate authority, or you can add your self-signed certificate to your trusted root store.
  + You might be using a certificate with a different subject name than the DNS name you are browsing to.  You can setup a DNS mapping (CNAME, A record, or local hosts file) to map your certificates subject name (for example, servicefabric.mycompany.com) to the Service Fabric management endpoint. (for example, mycluster.westus.cloudapp.azure.com), and then try browsing to your custom domain name (https://servicefabric.mycompany.com:19080/Explorer).
  + If you trust the server certificate that is presented, then you can just ignore the certificate warning in the browser and continue to the site.
  +	When connecting to a cluster which is secured by a certificate you must present a certificate in order to authenticate your client.  To do this make sure the cluster security certificate is in your personal certificate store.  When browsing to the management endpoint your web browser should prompt you to select a client certificate, at which time you can choose the cluster cert from your certificate store.
  +	If you are connecting with Powershell you need the cluster certificate in your personal certificate store, and you need to specify the client certificate in Powershell when connecting to the cluster. 
  
## **Recommended documents**
   [Connect to a secure cluster](https://azure.microsoft.com/documentation/articles/service-fabric-connect-to-secure-cluster/)
