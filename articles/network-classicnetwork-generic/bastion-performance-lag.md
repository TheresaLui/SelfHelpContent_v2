<properties
  pagetitle="Have a lag while using my RDP or SSH session"
  service="microsoft.network"
  resource="bastionhosts"
  ms.author="mariliu,taballa"
  selfhelptype="Generic"
  supporttopicids="32641419"
  resourcetags=""
  productpesids="16757"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="bastion-performance-lag"
  ownershipid="CloudNet_AzureBastion" />
# Have a lag while using my RDP or SSH session

## **Recommended Steps**

You may be using large number of RDP or SSH sessions on your Azure Bastion service. Both RDP and SSH are usage-based protocols, and a high usage of sessions will cause the bastion host to support a lower total number of sessions. Assuming normal day-to-day workflows, only 25 concurrent RDP sessions or 50 concurrent SSH sessions per deployment are supported currently.