<properties 
    pageTitle="How do I specify the ‘service’ and ‘protocol’ for an SRV record?"
    description="How do I specify the ‘service’ and ‘protocol’ for an SRV record?"
    service="microsoft.network"
    resource="dnszones"
    authors="jtuliani"
    displayOrder="5"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""​
    cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="ba47e559-bc22-4ed7-b914-2f6f600267ff"
	ownershipId="CloudNet_DNS"
/>

# How do I specify the ‘service’ and ‘protocol’ for an SRV record?

## **Recommended steps**

Azure DNS manages DNS records as record sets—the collection of records with the same name and the same type. For an SRV record set, the 'service' and 'protocol' need to be specified as part of the record set name. The other SRV parameters ('priority', 'weight', 'port' and 'target') are specified separately for each record in the record set.

Example SRV record names (service name 'sip', protocol 'tcp'):

- \_sip.\_tcp (creates a record set at the zone apex)
- \_sip.\_tcp.sipservice (creates a record set named 'sipservice')

## **Recommended documents**

[DNS zones and records](https://docs.microsoft.com/azure/dns/dns-zones-records)
<br>
[Create DNS record sets and records by using the Azure portal](https://docs.microsoft.com/azure/dns/dns-getstarted-create-recordset-portal)
<br>
[SRV record type (Wikipedia)](https://en.wikipedia.org/wiki/SRV_record)
