<properties
  pagetitle="WVD - Issues configuring your domain&#xD;"
  service=""
  resource=""
  ms.author="jerrycif,davidbel,evas"
  selfhelptype="Generic"
  supporttopicids="32783595"
  resourcetags=""
  productpesids="16582"
  cloudenvironments="blackforest,fairfax,public,usnat,ussec,mooncake"
  disableclouds=""
  articleid="53fb2b60-cfd0-4e5a-b9fb-f8bf83acc01d"
  ownershipid="Windows_Virtual_Desktop" />
# WVD - Issues configuring your domain

## Azure Windows Virtual Desktop: Issues configuring your domain

Most customers can resolve their issues using the following steps.

## **Recommended Steps**

* Make sure that multifactor authentication is not enabled for the account used to domain-join the virtual machines (VMs)
* Verify that the virtual network of the VMs has line-of-sight to the domain controller and that its DNS server points to the domain controller
* Review the [domain, user, and VM requirements](https://docs.microsoft.com/azure/virtual-desktop/overview#requirements) for Windows Virtual Desktop
* Review the [virtual machine details](https://docs.microsoft.com/azure/virtual-desktop/create-host-pools-azure-marketplace#virtual-machine-details) for the host pool creation
* [Review how to troubleshoot virtual machine configuration](https://docs.microsoft.com/azure/virtual-desktop/virtual-desktop-fall-2019/troubleshoot-vm-configuration-2019). Misconfiguration of the session host can cause a status of **unavailable**.

## **Recommended Documents**

* If you use Azure AD Domain Services, start with these [general troubleshooting steps](https://docs.microsoft.com/azure/active-directory-domain-services/troubleshoot)
* If your domain is on a separate virtual network than the virtual network you have access to, you may need to work with your network administrators to [configure virtual network peering](https://docs.microsoft.com/azure/virtual-network/virtual-network-peering-overview)
* Verify and troubleshoot [ExpressRoute connectivity](https://docs.microsoft.com/azure/expressroute/expressroute-troubleshooting-expressroute-overview)
