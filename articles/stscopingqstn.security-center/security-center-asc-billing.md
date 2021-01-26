<properties
  pagetitle="Security Center Billing self help guide&#xD;"
  ms.author="kawilson,elsagie"
  selfhelptype="Generic"
  supporttopicids="32693245,32693252"
  resourcetags=""
  productpesids="15947"
  cloudenvironments="public,fairfax,usnat,ussec,mooncake,blackforest"
  articleid="e5400786-b1c6-46a1-99e7-60666f4637dc"
  ownershipid="Azure_Security_Security_Center" />
# Security Center Billing self help guide

## **Recommended Steps**

**Why am I being billed? If I have Azure Defender for servers enabled at the subscription level, do I pay for servers that are not running?**  

No, Azure Security Center (ASC) charges hourly only for running servers. If a server is turned off, you won't pay for that server during the time that it's turned off. This applies to all other resource types protected by ASC, as well.

**Azure Defender for Servers is enabled on my subscription, but I didn't install the Log Analytics agent on this subscription's servers. Will I be charged for these machines?**

Azure VMs that are in a subscription with Azure Defender for enabled servers have capabilities even when the Log Analytics agent isn’t installed, including just-in-time access, network threat detection, regulatory compliance, and adaptive network hardening. Therefore, all Azure VMS in this subscription are charged. 

Learn more about [Azure Defender for servers](https://docs.microsoft.com/azure/security-center/defender-for-servers-introduction#what-are-the-benefits-of-azure-defender-for-servers).

Arc machines will be charged only if a Log Analytics agent is installed and reports data to a workspace with security or anti-malware solution installed

**If a Log Analytics agent is configured to send data to two different Log Analytics workspaces (multi-homing), will I be charged twice?**  

Yes, you'll be charged for each Log Analytics workspace that the agent reports to, assuming that the Log Analytics workspace has security or anti-malware solutions installed and the agent is up and running

**If a Log Analytics agent is configured to send data to two different log analytics workspaces (multi-homing), do I get the 500 MB of free Log Analytics ingestion benefit for each one of the reported Log Analytics workspaces?**  

Yes, the 500 MB of free ingestion is per node, per reported workspace, per day, assuming that the Log Analytics workspace has security or anti-malware solutions installed. If the ingested data exceeds 500 MB, you'll pay the extra amount

**Is the 500 MB of free data ingestion calculated for an entire workspace or strictly per machine?**  

You’ll get 500 MB of free data ingestion per day for every machine connected to the workspace, specifically for security data types directly collected by Azure Security Center. This data is a daily rate averaged across all nodes. So even if some machines send 100 MB and others send 800 MB, if the total doesn’t exceed the [number of machines] x 500 MB free limit, you won’t be charged extra.

## **Recommended Documents**

* [Billing questions](https://docs.microsoft.com/azure/security-center/faq-billing)
* [Pricing of Azure Defender](https://docs.microsoft.com/azure/security-center/security-center-pricing)

### Troubleshooting
* [ASC Troubleshooting Guide](https://docs.microsoft.com/azure/security-center/security-center-troubleshooting-guide)

### FAQ
* [ASC FAQ](https://docs.microsoft.com/azure/security-center/security-center-faq)
