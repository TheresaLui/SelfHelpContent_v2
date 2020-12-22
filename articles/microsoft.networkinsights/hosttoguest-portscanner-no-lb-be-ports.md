<properties
pageTitle="No Port Scan Results - Missing LB BE Ports"
description="No Port Scan Results - Missing LB BE Ports"
infoBubbleText="Port scan results for your resource. See details on the right."
service="microsoft.network"
resource="LoadBalancer"
authors="chadmat"
ms.author="chadmath"
displayOrder="10"
articleId="PortScanResultsNoLBPorts"
diagnosticScenario="PortScanResults"
selfHelpType="Diagnostics"
supportTopicIds="32436964,32436960,32582828,32582829,32582830,32582825,32582826,32582827,32582831,32582832,32436961,32573483,32582834,32436962,32565734,32565735,32565736,32582833"
resourceTags="windows"
productPesIds="16098"
cloudEnvironments="public, fairfax, usnat, ussec"
ownershipId="Cloudnet_NetworkWatcher"
/>
# No Port Connectivity Results - No LoadBalancer Backend Ports Detected
<!--issueDescription-->
We could not detect the load balancer backend port configuration for this load balancer. We could not continue validating the backend VM port communication. Follow the recommended steps below.
<!--/issueDescription-->

## **Recommended Steps**

1. Complete the configuration of the load balancer:
    - Validate that VMs exist in the [backend pool](https://docs.microsoft.com/azure/load-balancer/manage#backend-pools).
    - Validate that ports are listed in the **backend ports** of the [load balancing rules](https://docs.microsoft.com/azure/load-balancer/manage#load-balancing-rules)
    
2. After you verify that these settings have been completed and verified, run this diagnostic again in the **Diagnose and Solve** blade for this resource.


## **Recommended Documents**

* [Azure Load Balancer portal settings](https://docs.microsoft.com/azure/load-balancer/manage)
