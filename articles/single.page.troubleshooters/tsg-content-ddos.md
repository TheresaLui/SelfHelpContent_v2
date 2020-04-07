<properties pageTitle="DDoS Attack and Mitigation"
            description="DDoS Attack and Mitigation"
            service="Microsoft.Network"
            resource="Microsoft.Network/ddosProtectionPlans,Microsoft.Network/virtualNetworks"
            authors="JRMayberry"
            ms.author="rimayber"
            displayOrder=""
            selfHelpType="TSG_Content"
            supportTopicIds=""
            resourceTags=""
            productPesIds=""
            cloudEnvironments="public"
            articleId="df285fbc-0e84-423c-bc49-d75a32a2c6ed"
            ownershipId="Centennial_CloudNet_LoadBalancer" />

# Azure Networking - DDoS Protection


## Short Link
https://aka.ms/anpDdosWiki

## Recent Azure DDoS Protection [Work Items](https://aka.ms/anpworkitems)


## I'm Under Attack

If you are looking for guidance on an SR where a customer is actively undergoing a DDoS attack, please reference this wiki: [TSG: "I'm Under a DDoS Attack"](https://supportability.visualstudio.com/AzureNetworking/_wiki/wikis/Wiki/277561/TSG-I'm-Under-a-DDoS-Attack-)

## SR Processes

If you receive an SR in the Azure Networking POD that is NOT an "I'm Under Attack" SAP, the TAs & PG ask that you *always* post the SR into the [Azure DDoS channel](https://teams.microsoft.com/l/channel/19%3a9e0120d9ea8b479e8c603012f1b15e8f%40thread.skype/Azure%2520DDoS?groupId=c3e00ac7-3f76-4350-ba3b-e335a6bbbe21&tenantId=72f988bf-86f1-41af-91ab-2d7cd011db47) in the ANP Team in Teams. The PG has committed to assisting on every case possible, as DDoS is an extremely important technology offering to the Cloudnet PG. 

Even if you think you've got the answer the customer needs, please post to the channel for validation/verification.

## Feature Overview

The following feature overview was taken from [Azure DDoS Protection Standard overview](https://docs.microsoft.com/en-us/azure/virtual-network/ddos-protection-overview):  

Azure DDoS protection, combined with application design best practices, provide defense against DDoS attacks. Azure DDos protection provides the following service tiers:

- Basic: Automatically enabled as part of the Azure platform, at no additional charge. Always-on traffic monitoring, and real-time mitigation of common network-level attacks, provide the same defenses utilized by Microsoft’s online services. The entire scale of Azure’s global network can be used to distribute and mitigate attack traffic across regions. Protection is provided for IPv4 and IPv6 Azure public IP addresses.
- Standard: Provides additional mitigation capabilities over the Basic service tier that are tuned specifically to **Azure Virtual Network resources**. DDoS Protection Standard is simple to enable, and requires no application changes. Protection policies are tuned through dedicated traffic monitoring and machine learning algorithms. Policies are applied to public IP addresses associated to resources deployed in virtual networks, such as Azure Load Balancer, Azure Application Gateway, and Azure Service Fabric instances. Real-time telemetry is available through Azure Monitor views during an attack, and for history. Application layer protection can be added through the Azure Application Gateway Web Application Firewall. Protection is provided for IPv4 Azure public IP addresses.  
   - Note: **Azure Virtual Network resources** means ANY resources in the customer's Vnet, or resources *injected* into the customer's vnet. This includes things like:
      - Azure Public IP resources
      - Virtual Network Gateways (VPN & ExR)
      - Azure Firewalls
      - Web App App Service Environments (NOT vnet-connected via P2S, but actual ASEs)
      - Azure Bastion Hosts
      - Azure Application Gateways

The DDoS PG also maintains an internal set of documents about how DDoS works, FAQs, etc:

- [Internal DDoS Docs Home](https://microsoft.sharepoint.com/teams/AzureDDOSProtection/SitePages/Home.aspx) or <https://aka.ms/ddos>
- [How Azure DDoS Protection Works](https://microsoft.sharepoint.com/teams/AzureDDOSProtection/SitePages/How-Azure-DDoS-Protection-Works.aspx)
- [List of Mitigations Provided by Azure DDoS Protection](https://microsoft.sharepoint.com/teams/AzureDDOSProtection/SitePages/List-of-Mitigations.aspx)
- [Analysis of Well-Known BotNets](https://microsoft.sharepoint.com/teams/AzureDDOSProtection/SitePages/Protection-Against-Well-Known-BotNets.aspx)
- [Frequently Asked Questions](https://microsoft.sharepoint.com/teams/AzureDDOSProtection/SitePages/Frequently-Asked-Questions.aspx)
- [DDoS Extortion Response Guidelines](https://microsoft.sharepoint.com/teams/AzureDDOSProtection/SitePages/DDoS-Extortion-Response-Guidelines.aspx)

## Architecture Diagram


## Public Documentation

- **Overview**  
  - Feature Overview: [Azure DDoS Protection Standard overview](https://docs.microsoft.com/en-us/azure/virtual-network/ddos-protection-overview)
  - Configure/Manage: [Manage Azure DDoS Protection Standard using the Azure portal](https://docs.microsoft.com/en-us/azure/virtual-network/manage-ddos-protection)
- **Announcements**  
  - Azure Updates page for Azure DDoS Protection: [Azure Updates \#Azure DDoS Protection](https://azure.microsoft.com/en-us/updates/?product=ddos-protection&status=all)
  - GA (4/18/2018): [Azure DDoS Protection for virtual networks generally available](https://azure.microsoft.com/en-us/blog/azure-ddos-protection-for-virtual-networks-generally-available/) or (<https://aka.ms/ddosblog>)
  - Public Preview (9/25/2017): [Azure DDoS Protection Service preview](https://azure.microsoft.com/en-us/blog/azure-ddos-protection-service-preview/)

## Training and Other Resources

- Feature Friday: [Azure DDoS Protection Feature Friday (folder)](https://microsoft.sharepoint.com/:f:/r/teams/WAG/AzureNetworking/aznetcce/Shared%20Documents/Feature%20Friday/Azure%20DDoS?csf=1&e=NF70y0)
  - [180713 Feature Friday - Azure DDoS Protection Americas - Friday, July 13, 2018 12.33.25 PM](https://microsoft.sharepoint.com/:v:/r/teams/WAG/AzureNetworking/aznetcce/Shared%20Documents/Feature%20Friday/180713%20Feature%20Friday%20-%20Azure%20DDoS%20Protection%20Americas%20-%20Friday,%20July%2013,%202018%2012.33.25%20PM.mp4?csf=1&e=Nsg7aS)
  - [180713 Feature Friday - Azure DDoS Protection APAC - Friday, July 13, 2018 9.32.29 AM](https://microsoft.sharepoint.com/:v:/r/teams/WAG/AzureNetworking/aznetcce/Shared%20Documents/Feature%20Friday/180713%20Feature%20Friday%20-%20Azure%20DDoS%20Protection%20APAC%20-%20Friday,%20July%2013,%202018%209.32.29%20AM.mp4?csf=1&e=RN0CR3)
- Brownbags:
  - [DDoS Protection Mitigation Reports and Flow Logs (DDoS Attack Analysis - Date delivered: 20180921](https://microsoft-my.sharepoint.com/:v:/p/bbenson/EbizCTlC9PNKtdvb1hjgwZsBl-xsUVMm59M7WwsRelZxoA?e=hCdLb6)
- Older Training Sources:
  - OneNote: [DDoS Protection OneNote Web view](https://microsoft.sharepoint.com/teams/CSSSecIR/_layouts/OneNote.aspx?id=%2Fteams%2FCSSSecIR%2FSiteAssets%2FDDOS%20-%20Secure%20Virtual%20Networking%20CSS%20OneNote&wd=target%28Support.one%7C393BAE14-B069-43D6-9C58-5804270470EE%2F%29)
  - Learning path: <https://ready.azurewebsites.net/services/2005>
- [Azure Friday - Azure DDoS Protection](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fmsit.microsoftstream.com%2Fvideo%2F86937ff9-ac2f-404f-bc4e-e87c002d0ef3&data=02%7C01%7CRyan.Borstelmann%40microsoft.com%7C85f1f92cb44849402c1a08d75975dc05%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637076235097473822&sdata=8wbi2W7HlegwoVXS405g7ciyabHK7pHaM%2F%2Bv%2B3JKceg%3D&reserved=0)

## Azure DDoS Protection Reporting

- **P360: Azure DDoS Protection**
  - Azure DDoS Protection:
    - [P360 \> Azure DDoS Protection\> ClosedVolume \> ByProblemType-RCLvl3 \> Monthly](https://product360.msftcloudes.com/product/643/domain/Support?meter=Microsoft.Cloud.P360.SupportDomain.Production.ClosedVolume_33287&filters=%7B%22filters%22:%5B%5D%7D&period=Month)
 
    