<properties
  pagetitle="Issues and questions with DNS and connectivity."
  description="Resolve difficulties with private IP or configuring private DNS."
  service=""
  resource=""
  ms.author="mariliu"
  selfhelptype="Generic"
  supporttopicids="32788104"
  resourcetags=""
  productpesids="16843"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="13a17fa9-c016-4468-b787-0f2c94d8e450"
  ownershipid="CloudNet_PrivateLink" />
# Issues and questions with DNS and connectivity.

## **Recommended Steps**

1. Review the Private Endpoint (PE) configuration:

   * The PE must be in an approved and succeeded state.
   * Ensure that the fully qualified domain name (FQDN) is assigned properly, with **A record** (a basic type of domain name service (DNS) record) and **CName**.
   * The client virtual machine (VM) virtual network must be associated with the private zone.

2. Validate the DNS connection health by using Azure [Network Watcher](http://docs.microsoft.com/azure/network-watcher/network-watcher-monitoring-overview#monitor-communication-between-a-virtual-machine-and-an-endpoint).

3. Verify that you are using a private Domain Name Service(DNS) Zone.

4. If you are using a custom DNS, verify that:

   * The custom DNS Server is forwarding all requests to the Azure provided DNS internet protocol (IP), **168.63.129.16**.
   * The source VM has IP connectivity to VNet.

## **Recommended Documents**

Troubleshooting connectivity issues

- [Troubleshoot Azure Private Endpoint connectivity problems](http://docs.microsoft.com/azure/private-link/troubleshoot-private-endpoint-connectivity)
- [Troubleshoot Private Link Service connectivity problems](http://docs.microsoft.com/azure/private-link/troubleshoot-private-link-connectivity)
- [Use Azure Firewall to inspect traffic destined to a private endpoint](https://docs.microsoft.com/azure/private-link/inspect-traffic-with-azure-firewall)

Frequently-used links 
- [Azure Private Endpoint DNS configuration](http://docs.microsoft.com/azure/private-link/private-endpoint-dns)
- [Integrate with Private DNS](https://github.com/dmauser/PrivateLink/tree/master/DNS-Integration-Scenarios)
- [Build DNS Forwarder](https://github.com/Microsoft/PL-DNS-Proxy)
- [DNS Configuration Using Active Directory](https://github.com/dmauser/PrivateLink/tree/master/DNS-Scenario-Using-AD)
- [Azure DNS Limits](http://docs.microsoft.com/azure/azure-resource-manager/management/azure-subscription-service-limits#azure-dns-limits)
- [Private Link limits](http://docs.microsoft.com/azure/azure-resource-manager/management/azure-subscription-service-limits#private-link-limits)