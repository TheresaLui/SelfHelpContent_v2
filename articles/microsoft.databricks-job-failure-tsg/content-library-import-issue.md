<properties
	pageTitle="Library import issue"
	description="Library import issue"
	service=""
	resource=""
	authors="rimayber"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="b0e026bb-d129-4608-b2c7-7c2904712583"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Library import issue

Jobs can be run on either existing or new cluster. Please double check the following in Job and Cluster configuration:

1. If Job is run on Existing Cluster, when restarting with libraries, the job WILL NOT WAIT for library installation.
2. If Job is run on New Cluster with a shared library (a library installed on all clusters), the job WILL NOT WAIT for library installation.

Provide customer with ready message below.
