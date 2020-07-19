<properties 
    pageTitle="I can't create a DNS record"
    description="I am unable to create a new DNS record in my DNS zone in Azure DNS."
    service="microsoft.network"
    resource="dnszones"
    authors="jtuliani"
    displayOrder="2"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""​
    cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="9b399a45-3013-4f64-b583-eeae56c6da88"
	ownershipId="CloudNet_DNS"
/>

# I can't create a DNS record

## **Recommended steps**

To resolve common issues, try one or more of the following:

1.	Review [Audit logs](data-blade:Microsoft_Azure_Insights.AzureDiagnosticsBladeWithParameter) to determine the failure reason.
2.	Does the record set exist already?  Azure DNS manages records using record *sets*, which are the collection of records of the same name and the same type. If a record with the same name and type already exists, then to add another such record you should edit the existing record set.
3.	Are you trying to create a record at the DNS zone apex (the ‘root’ of the zone)? If so, the DNS convention is to use the ‘@’ character as the record name. Also note that the DNS standards do not permit CNAME records at the zone apex.
4.	Do you have a CNAME conflict?  The DNS standards do not allow a CNAME record with the same name as a record of any other type. If you have an existing CNAME, creating a record with the same name of a different type fails.  Likewise, creating a CNAME fails if the name matches an existing record of a different type. Remove the conflict by removing the other record or choosing a different record name.
5.	Have you reached the limit on the number of record sets permitted in a DNS zone? The current number of record sets and the maximum number of record sets are shown in the Azure portal, under the 'Properties' for the zone. If you have reached this limit, then either delete some record sets or contact Azure Support to raise your record set limit for this zone, then try again. 

If the above steps don't resolve the issue, please post this issue to our [community support forum on MSDN](https://social.msdn.microsoft.com/Forums/en-US/home?forum=WAVirtualMachinesVirtualNetwork) or open an Azure support request.

## **Recommended documents**

[DNS zones and records](https://docs.microsoft.com/azure/dns/dns-zones-records)
<br>
[Create DNS record sets and records by using the Azure portal](https://docs.microsoft.com/azure/dns/dns-getstarted-create-recordset-portal)
