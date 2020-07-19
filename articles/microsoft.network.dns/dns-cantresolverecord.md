<properties 
    pageTitle="I can't resolve my DNS record"
    description="I am unable to resolve a new DNS record in a DNS zone hosted in Azure DNS."
    service="microsoft.network"
    resource="dnszones"
    authors="jtuliani"
    displayOrder="3"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
    cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="c6e1cc06-8886-4bf5-afd5-f8e03df81d3e"
	ownershipId="CloudNet_DNS"
/>

# I can't resolve my DNS record

## **Recommended steps**

DNS name resolution is a multi-step process, which can fail for many reasons. The following steps help you investigate why DNS resolution is failing for a DNS record in a zone hosted in Azure DNS.

1.	Confirm that the DNS records have been configured correctly in Azure DNS. Review the DNS records in the Azure portal, checking that the zone name, record name, and record type are correct.
2.	Confirm that the DNS records resolve correctly on the Azure DNS name servers.
    - If you make DNS queries from your local PC, you may see cached results that don’t reflect the current state of the name servers.  Also, corporate networks often use DNS proxy servers, which prevent DNS queries from being directed to specific name servers.  To avoid these problems, use a web-based name resolution service such as [digwebinterface](http://digwebinterface.com).
    - Be sure to specify the correct name servers for your DNS zone, as shown in the Azure portal.
    - Check that the DNS name is correct (you have to specify the fully qualified name, including the zone name) and the record type is correct
3.	Confirm that the DNS domain name has been correctly [delegated to the Azure DNS name servers](https://docs.microsoft.com/azure/dns/dns-domain-delegation). There are a [many 3rd-party web sites that offer DNS delegation validation]( https://www.bing.com/search?q=dns+check+tool). This test is a *zone* delegation test, so you should only enter the DNS zone name and not the fully qualified record name.
4.	Having completed the above, your DNS record should now resolve correctly. To verify, you can again use [digwebinterface](http://digwebinterface.com), this time using the default name server settings.

If the above steps don't resolve the issue, please post this issue to our [community support forum on MSDN](https://social.msdn.microsoft.com/Forums/en-US/home?forum=WAVirtualMachinesVirtualNetwork) or open an Azure support request.

## **Recommended documents**

[Delegate a domain to Azure DNS](https://docs.microsoft.com/azure/dns/dns-domain-delegation)


