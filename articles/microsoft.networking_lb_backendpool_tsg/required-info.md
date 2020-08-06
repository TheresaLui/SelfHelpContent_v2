<properties
	pageTitle="Check scope and required information"
	description="Check scope and required information"
	service="microsoft.network"
	resource="loadBalancers"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds="32588977"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="304ab667-c4ca-4f70-9bb7-e4723237eb4c"
	ownershipId="CloudNet_LoadBalancer"
/>

# How to check scope and required information

## **Recommended Steps**

Be sure you have the required information to effectively investigate and the proceed with the TSG. This information can be obtained from Azure Support Center or the SR customer verbatim that has the scoping questions.

* Subscription ID
* Resource Group
* Load balancer name
* Load balancer backend pool name
* Frontend IP and Port
* Source IP connecting to the load balancer
* Are the VMs experiencing a connectivity issue part of the LB backend pool
* Whether this is a live issue or a request for an RCA
* The result of the customer bypassing the LB directly to backend
