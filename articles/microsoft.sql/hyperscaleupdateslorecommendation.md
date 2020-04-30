<properties
 pageTitle="Hyperscale I/O Bottleneck" description="Hyperscale I/O Bottleneck"
 infoBubbleText="Found recent high I/O usage on your hyperscale database. See details on the right." 
 service="microsoft.sql"
 resource="servers"
 authors="ManojRajandrakumar"
 ms.author="marajand"
 displayOrder=""
 articleId="HyperscaleIO_94b1a74b-a663-4d09-8ce1-735122a4e261"
 diagnosticScenario="SqlHyperScale"
 selfHelpType="diagnostics"
 supportTopicIds="32632131"
 resourceTags=""
 productPesIds="13491"
 cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLDB_Provisioning"
/>

# We ran diagnostics on your resource and found an issue
<!--issueDescription-->
We see high I/O usage on your Hyperscale database<!--$DatabaseName-->DatabaseName<!--/$DatabaseName--> on server <!--$ServerName-->ServerName<!--/$ServerName-->. This is likely due to data exceeding the size of the RBPEX cache on the Compute Node, which leads to an increased number of remote requests to Page Servers to fetch data pages.
<!--/issueDescription-->

## **Recommended Steps**

* Scale to a higher service tier, which will increase the size of the RBPEX leading to less remote I/O requests
* If you are facing a performance degradation, try having a less aggressive workload

## **Recommended Documents**

* [Upgrade to Higher SLO]( https://docs.microsoft.com/previous-versions/azure/dn369872(v=azure.100))
* [Hyperscale Architecture](https://www.microsoft.com/research/uploads/prod/2019/05/socrates.pdf)
