<properties
  pagetitle="Windows Virtual Desktop - Issues configuring your domain&#xD;"
  service=""
  resource=""
  ms.author="jerrycif,davidbel,evas"
  selfhelptype="Generic"
  supporttopicids="32783595"
  resourcetags=""
  productpesids="16582"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="53fb2b60-cfd0-4e5a-b9fb-f8bf83acc01d"
  ownershipid="Windows_Virtual_Desktop" />
# Windows Virtual Desktop - Issues configuring your domain

## **Recommended Steps**

* Ensure the account used to domain join the VMs does not have multifactor authentication enabled
* Verify that the virtual network of the VMs has line-of-sight to the domain controller and it's DNS server points to the domain controller
* Review the [domain, user and VM requirements](https://docs.microsoft.com/azure/virtual-desktop/overview#requirements) for Windows Virtual Desktop
* Review the [virtual machine details](https://docs.microsoft.com/azure/virtual-desktop/create-host-pools-azure-marketplace#virtual-machine-details) for the host pool creation

## **Recommended Documents**

* If you are using Azure AD Domain Services, begin with these [general troubleshooting steps](https://docs.microsoft.com/azure/active-directory-domain-services/troubleshoot)
* If your domain is on a separate virtual network than the virtual network that you have access to, you may need to work with your network administrators to configure [virtual network peering](https://docs.microsoft.com/azure/virtual-network/virtual-network-peering-overview)
* Verify and troubleshoot [ExpressRoute connectivity](https://docs.microsoft.com/azure/expressroute/expressroute-troubleshooting-expressroute-overview)