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

<!--issueDescription-->

Jobs can be run on either existing or new cluster. Please double check the following in Job and Cluster configuration:<br>
<br>
1. If Job is run on Existing Cluster, when restarting with libraries, the job WILL NOT WAIT for library installation.<br>
2. If Job is run on New Cluster with a shared library (a library installed on all clusters), the job WILL NOT WAIT for library installation.<br>
<br><br>
**Solution**<br>
<br>
If a job requires a certain library, make sure to attach the library to the job itself, not the cluster.<br>

<!--/issueDescription-->

## Recommended document(s)

1. [Jobs Library Dependancies](https://docs.microsoft.com/azure/databricks/jobs#library-dependencies)