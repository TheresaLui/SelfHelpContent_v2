<properties
pageTitle="Solution: No platform issues found"
description="Solution: No platform issues found"
infoBubbleText="Solution: No platform issues found"
service="microsoft.network"
ownershipId="Centennial_Cloudnet_VirtualNetwork"
resource="virtualnetwork"
authors="chadmath"
ms.author="chadmat"
displayOrder=""
articleId="SolutionNoPlatformIssuesFound"
diagnosticScenario="SolutionNoPlatformIssuesFound"
selfHelpType="TSG_Content"
supportTopicIds=""
resourceTags="windows"
productPesIds="15526"
cloudEnvironments="Public, Fairfax, usnat, ussec"
/>
# Resources and underlying platform show healthy
<!--issueDescription-->

We've checked the resource health and the platform health at the time of the reported issue. The resources involved and the underlying platform are showing healthy at the reported time. Due to our inability to reproduce the issue and all VM and platform health checks are ok at the time reported, we are unable to determine what may have caused the reported symptoms. It is possible it could have been caused by an issue with the application on the VM or another anomaly. We are sorry for any inconvenience this may have caused! We've provided some tooling below that may help if you experience an issue like this in the future.

<!--/issueDescription-->

## **Recommended Steps**

1. Check the VNet Peering status on the 'peerings' tab in each VNet involved. If the status shows connected then the VNet peering connectivity is ok.
2. Check the resource health for all resources involved by going to the resource 'Overview' tab to check on CPU, Disk and Network signals. 
3. Remote into the VMs to ensure the applications are working as expected
4. Use the Network Watcher toolset to check connectivity between resources (linked below)

## **Recommended Documents**

* [Diagnose VM Network Traffic Filter Problem](https://docs.microsoft.com/azure/network-watcher/diagnose-vm-network-traffic-filtering-problem)
* [Diagnose VM routing problems](https://docs.microsoft.com/azure/network-watcher/network-watcher-next-hop-overview)
