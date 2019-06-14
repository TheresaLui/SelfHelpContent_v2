<properties
	pageTitle="Management/Service level or performance tier change"
	description="Management/Service level or performance tier change"
	service="microsoft.sql"
	resource="servers"
	authors="rohitnayakmsft"
    ms.author="rohitna"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32594732"
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="public"
	articleId="27976eaa-1b1e-46e7-82c9-395b9f9ad81e"
/>
# Service level or performance tier change

## **Recommended Steps**

* Applications hosted on Managed Instance can leverage Azure platform elasticity through the online update service tier operation, which allows independent scaling of compute and storage ranging from 8 to 80 vCores and from 32GB to 8TB respectively. Also, changing the service tier from General Purpose to Business Critical and vice versa, without application downtime, according to the workload’s requirements.<br> 
* You can view status of operation in your activity log. Resizing related to Business Critical service tear may require size-of-data operations and take more time.<br>
* Read more about [Managed Instance service tiers](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance#managed-instance-service-tiers)<br>
