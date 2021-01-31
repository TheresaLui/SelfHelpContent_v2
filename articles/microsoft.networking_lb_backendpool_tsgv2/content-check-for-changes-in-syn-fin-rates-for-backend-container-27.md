<properties
	  pageTitle="Check for changes in SYN/FIN rates for backend container"
	  description="Check for changes in SYN/FIN rates for backend container"
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
	  articleId="d7e1b412-5b57-4a33-929b-6ff5223b8591"
	  ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Check for changes in SYN/FIN rates for backend container

Look at the VfpTcpMetricsDashboard for backend pool member to see if there is a spike of TCP SYN or FIN packets at the time of the reported incident.

Such spikes in activity can indicate an application failure. If the application fails and restarts, clients will need to re-connect. When TCP based clients connect, they trigger SYN packets as part of the protocol?s 3-way handshake. Look for a spike in inbound TcpSyn or TcpFin packets. If so, that points to what is likely a customer application issue.

## Recommended Steps
1. In ASC, browse to a member of the backend pool. In the VM?s properties, make note of:
* Region
* Cluster
* NodeId
* ContainerId
2. Browse to URL: https://jarvis-west.dc.ad.msft.net/dashboard/VfpMDM/DatapathDashboards/VfpTcpMetricsDashboard
3. At the top where the parameters are, set the time to on hour before and after the time of the incident. For Account, specify VfpMdm<region> where region is typically the first two letters of the cluster. There are some exceptions however listed below:

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

Then specify the cluster name, node Id, and container Id.

