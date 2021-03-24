<properties
 pageTitle="Check DDoS dashboard to see if customer VIP was under mitigation"
 description="Check DDoS dashboard to see if customer VIP was under mitigation"
 service="Microsoft.Network"
 resource="Microsoft.Network/loadBalancers"
 authors="Centennial_CloudNet_LoadBalancer"
 ms.author="Centennial_CloudNet_LoadBalancer"
 displayOrder=""
 selfHelpType="TSG_Content"
 supportTopicIds=""
 resourceTags=""
 productPesIds=""
 cloudEnvironments="public, fairfax, usnat, ussec"
 articleId="5860459b-288b-4d11-aae6-d5486415d637"
 ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Check DDoS dashboard to see if customer VIP was under mitigation

The DDoS system monitors all Microsoft IP space at all network edge sites to prevent attack traffic from saturating the network internally and to protect the load balancer inbound MUX rings from bad actors on the internet. If inbound traffic rates exceed attack thresholds, the DDoS system filters the traffic. By default, all customers are enrolled in DDoS protection basic. Customers can opt into DDoS Protection Standard for an additional charge. DDoS Protection standard offers customers the ability to tune mitigation policies for their application, metrics and alerts, and mitigation reports and flow logs, among other features.

## Recommended Steps for checking if VIP was under mitigation

1. Load the DDoS mitigation dashboard here: https://jarvis-west.dc.ad.msft.net/dashboard/CNS/DDoSSupport/IsIPUnderMitigation
2. In the gray override bar at the top, adjust the time to the time of the incident. Keep in time zones in mind. It is recommended to set Jarvis to use UTC (set this by clicking on the person icon in the upper right-hand corner of Jarvis) and convert the customer's incident time to UTC. Enter the customer's VIP in the DestinationVIP box.

If you do not see the customer's VIP or no data appears, the customer's VIP was not under mitigation and therefore was not under attack.

## Recommended Documents
https://docs.microsoft.com/en-us/azure/ddos-protection/ddos-protection-overview