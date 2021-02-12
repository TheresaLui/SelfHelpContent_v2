<properties
pageTitle="Solution NVA Referral"
description="Solution NVA Referral"
infoBubbleText="Solution NVA Referral"
service="microsoft.network"
resource="virtualnetwork"
authors="chadmath"
ms.author="chadmat"
displayOrder=""
articleId="SolutionNVAReferral"
diagnosticScenario="SolutionNVAReferral"
selfHelpType="TSG_Content"
supportTopicIds=""
resourceTags="windows"
productPesIds="15526"
cloudEnvironments="Public, fairfax, usnat, ussec"
ownershipId="Centennial_Cloudnet_VirtualNetwork"
/>
# Network Virtual Appliance (NVA) blocking traffic
<!--issueDescription-->

We have identified your network virtual appliance (NVA) VM configuration as the likely cause of the connectivity issue by validating the following Azure platform requirements:

* You must use a Network Virtual Appliance (NVA) in the Hub Vnet
* There must be UDRs in the spoke VNets with the next hop type of 'Network Virtual Appliance' pointing to the NVA private VNet IP
* NVA NICs must have *'IP Forwarding'* enabled <br><br>

The last remaining requirement is that *NVAs must be configured correctly internally*. For that, we ask that you [contact the vendor of the NVA or NVA software](https://support.microsoft.com/help/2984655/support-for-azure-market-place-for-virtual-machines)  


<!--/issueDescription-->

## **Recommended Steps**

1. [Contact the vendor of the NVA or NVA software](https://support.microsoft.com/help/2984655/support-for-azure-market-place-for-virtual-machines)
2. Provide the NVA vendor with the following resource: [Check the minimum configuration requirements for NVAs](https://docs.microsoft.com/azure/virtual-network/virtual-network-troubleshoot-nva#check-the-minimum-configuration-requirements-for-nvas-on-azure)

## **Recommended Documents**

* [NVA Troubleshooter](https://docs.microsoft.com/azure/virtual-network/virtual-network-troubleshoot-nva)
* [NVA Vendor contact information](https://support.microsoft.com/help/2984655/support-for-azure-market-place-for-virtual-machines)

