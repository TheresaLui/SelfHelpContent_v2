<properties 
    pageTitle="I can't create a new DNS record in private DNS zone"
    description="I am unable to create a new DNS record in my private DNS zone."
    service="microsoft.network"
    resource="privateDnsZones"
    authors="rohinkoul"
    ms.author="rohink"
    displayOrder="2"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
    cloudEnvironments="public,fairfax,mooncake,blackforest, usnat, ussec"
	articleId="privatedns-cantcreaterecord"
	ownershipId="CloudNet_DNS"
/>

# I can't create a new DNS record

## **Recommended Steps**

To resolve common issues, try one or more of the following:

* Review [Audit logs](data-blade:Microsoft_Azure_Insights.AzureDiagnosticsBladeWithParameter) to determine the failure reason
* Does the recordset exist already?  Azure DNS manages records using record *sets*, which are the collection of records of the same name and the same type. If a record with the same name and type already exists, then to add another such record you should edit the existing recordset.
* Are you trying to create NS records? Azure DNS private zones do not support creation of NS (Name Server) records. If you intend to create a child zone simply create the child zone and link it to the virtual network. You don't need to add NS delegations in parent zone.
* Are you trying to create a resource record for a virtual machine? Please check if you have enabled auto registration for virtual machine resource records. When auto registration is enabled Azure DNS automatically creates resource records for the virtual machines hosted in a linked virtual network. If you try to create same record again you will get an error. You can either disable auto registration or create the resource record with a different name.
* Are you trying to create a record at the DNS zone apex (the ‘root’ of the zone)? If so, the DNS convention is to use the ‘@’ character as the record name. Also note that the DNS standards do not permit CNAME records at the zone apex.
* Do you have a CNAME conflict?  The DNS standards do not allow a CNAME record with the same name as a record of any other type. If you have an existing CNAME, creating a record with the same name of a different type fails.  Likewise, creating a CNAME fails if the name matches an existing record of a different type. Remove the conflict by removing the other record or choosing a different record name.
* Have you reached the limit on the number of recordsets permitted in a DNS zone? The current number of recordsets and the maximum number of recordsets are shown in the Azure portal, under the 'Properties' for the zone. If you have reached this limit, then either delete some recordsets or contact Azure Support to raise your recordset limit for this zone, then try again.
* In order to make changes to a private DNS zone you must have appropriate [RBAC](https://docs.microsoft.com/azure/role-based-access-control/overview) permissions. Please make sure you have "Private DNS Zone Contributor" Role assigned.

## **Recommended Documents**

* [Create Azure DNS private zones and records](https://docs.microsoft.com/azure/dns/private-dns-portal)
