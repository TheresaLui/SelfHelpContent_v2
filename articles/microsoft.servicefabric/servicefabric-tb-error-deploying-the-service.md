<properties 
	pageTitle="Errors deploying a service" 
	description="Errors deploying a service " 
	service="microsoft.servicefabric"
	resource="servicefabric"
	authors="pkcsf"
	displayOrder="6"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="servicefabric"
	productPesIds=""
	cloudEnvironments="public"	 
/>
 
# Errors deploying a service 

##**Recommended steps**
1. The majority of deployment failures are caused by exceptions when a service is starting. This could be a missing dependency or exception in the constructor, or an exception in one of the Service Fabric startup methods (RunAsync, OnActivateAsync, CreateServiceReplicaListeners, CreateServiceInstanceListeners). See the ‘Common Failures and Troubleshooting Steps for Application/Service' section for how to troubleshoot.
2. Verify that your instance/replica count does not exceed the size of your cluster.

