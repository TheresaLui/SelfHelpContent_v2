<properties
 pageTitle="Check for changes in SYN/FIN rates for backend container"
 description="Check for changes in SYN/FIN rates for backend container"
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
 articleId="12ba81d0-4828-474b-9388-3ccffde8f183"
 ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Check for changes in SYN/FIN rates for backend container

Look at the VfpTcpMetricsDashboard for backend pool member. Look at the VfpTcpMetricsDashboard for backend pool member to see if there is a spike of TCP SYN or FIN packets at the time of the reported incident.

Such spikes in activity can indicate an application failure. If the application fails and restarts, clients will need to re-connect. When TCP based clients connect, they trigger SYN packets as part of the protocol’s 3-way handshake. Look for a spike in inbound TcpSyn or TcpFin packets. If so, that points to what is likely a customer application issue.

## Recommended Steps
1. In ASC, browse to a member of the backend pool. In the VM’s properties, make note of:
* Region
* Cluster
* NodeId
* ContainerId
2. Browse to URL: https://jarvis-west.dc.ad.msft.net/dashboard/VfpMDM/DatapathDashboards/VfpTcpMetricsDashboard
3. At the top where the parameters are, set the time to on hour before and after the time of the incident. For Account, specify VfpMdm[Region] where region is typically the first two letters of the cluster. VfpMdmSN for SN#PrdApp## clusters in US South Central for example. There are some exceptions however listed below:

Cluster Starts With | Vfp Account Parameter
--- | ---
MNZ | VfpMdmBL
MEL | VfpMdmML
CO | VfpMdmMWH
BZ | VfpMdmBN
AUH | VfpMdmAUHDXB
DXB | VfpMdmAUHDXB
DUB | VfpMdmDB
KW | VfpMdmKWTY
TY | VfpMdmKWTY
SIN | VfpMdmSG
DSM | VfpMdmDM

Then specify the cluster name, node Id, and container Id. Often times, it is easier to construct the URL off-line with the parameters pre-populated: `https://jarvis-west.dc.ad.msft.net/dashboard/VfpMDM/DatapathDashboards/VfpPortMetricsDashboard?overrides=[{"query":"//dataSources","key":"account","replacement":"*VFP Account*"},{"query":"//*[id='Cluster']","key":"value","replacement":"*Cluster Name*"},{"query":"//*[id='NodeId']","key":"value","replacement":"*Node Id*"},{"query":"//*[id='ContainerId']","key":"value","replacement":"*Container Id*"}]%20`