<properties
    pageTitle="Orcas MariaDB server is facing slow login issues"
    description="Orcas MariaDB server is facing slow login issues"
    infoBubbleText="Server is facing slow login issues. See details on the right"
    service="microsoft.dbformariadb"
    resource="dbformariadb"
    authors="congwang"
    ms.author="conwan"
    displayOrder="100"
    articleId="dbformariadb-asc-performance-slowlogin"
    diagnosticScenario="OrcasMariaDBSlowLogin"
    selfHelpType="rca"
    resourceTags="servers, databases"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforMariaDB"
/>

# Server is facing slow login issues

<!--issueDescription-->
During our investigation regarding performance issues to your MariaDB server <!--$ServerName-->ServerName<!--/$ServerName--> we found that 70% of login setup time is above 1 second between <!--$StartTime-->StartTime<!--/$StartTime--> and <!--$EndTime-->EndTime<!--/$EndTime--> (UTC). Slow login issues can have many different root causes.
<!--/issueDescription-->

## **Recommended Steps**

* Monitor the resource consumption of your server. If you are maxing out IO, memory or compute resources, scale up the resource that you are limited on.
* If your client is hosted in an Azure VM, use accelerated networking for lowest connection latency. Please see the recommended documents section. 
* In order to avoid overhead for establishing new connections, consider using a connection pooler between your application and MariaDB server.

## **Recommended Documents**

* [Accelerated networking for Linux VMs](https://docs.microsoft.com/azure/virtual-network/create-vm-accelerated-networking-cli)<br>
* [Accelerated networking for Windows VMs](https://docs.microsoft.com/azure/virtual-network/create-vm-accelerated-networking-powershell)