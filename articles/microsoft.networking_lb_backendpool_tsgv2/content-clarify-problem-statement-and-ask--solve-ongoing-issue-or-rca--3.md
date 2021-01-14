<properties
	  pageTitle="Clarify problem statement and ask (solve ongoing issue or RCA)"
	  description="Clarify problem statement and ask (solve ongoing issue or RCA)"
    service="Microsoft.Network"
     resource="Microsoft.Network/loadBalancers"
	  authors="dgoddard"
	  ms.author="dgoddard"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="cf621958-40ba-47f5-a50f-969f7039c7d2"
	  ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Clarify problem statement and ask (solve ongoing issue or RCA)

Most customers are asking to help them understand why they are not currently getting responses to requests to their load balancer frontend IP or why they failed in the past. Often, customer's report that their load balancer is "down" but do not check to see if their application is/was healthy or is misconfigured.

## Recommended Steps

1. Review the customer verbatim to understand the customer's ask.
2. Locate the customer's load balancer in ASC. Determine from the verbatim where the customer is connecting from. This should be either a public IP address in the case of external facing load balancers or a VNet IP, resource URI, or on-premises IP for internal load balancers.  From the configuration data is visualized in ASC and what you have read from the customer verbatim, collect the following information to form a concise problem statement:

1. Client IP (source):
2. Load balanced frontend IP, port, and protocol (TCP or UDP - other protocols such as ICMP are not supported) client is connecting to (destination): 
3. Load balanced rule the customer configured for the traffic pattern: 
4. Probe configuration associated with the load balanced rule: 
5. Load balancer SKU (standard or basic): 
6. If intermittent/RCA request, date and time in UTC of the incident: 

