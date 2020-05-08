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
            cloudEnvironments="public, fairfax, usnat, ussec"
            articleId="8dbeff99-8396-4c14-bdc2-3c5040dfdf30"
            ownershipId="Centennial_CloudNet_LoadBalancer" />


First, determine if the customer is using DDoS Protection Standard SKU or not. This is very [easy to do](https://supportability.visualstudio.com/AzureNetworking/_wiki/wikis/Wiki/300601/TSG-Determine-Customer's-DDoS-SKU). It can be located in ASC as a resourceType for quick identification. If you see Microsoft.Network/ddosProtectionPlans listed in ASC, it's DDoS Protection Standard customer.

**Important**: If the customer has an ARR support contract then the case will stay with ARR regardless of DDoS Basic or Standard.  Please check this before sending to the PODs.

**NOTE:** Anything under 10k packets/sec is NOT considered a DDoS by Microsoft's definition. Customers will need to scale their resources to handle this, as DDoS Protection Standard cannot protect below this figure.

**NOTE:** Azure also currently provides protection against layer 3 (L3) and layer 4 (L4) DDoS attacks, which include TCP SYN, New Connections, UDP/ICMP/TCP floods. All Azure endpoint VIPs (/32) are guarded at platform safe thresholds. The protection extends to traffic flows inbound from the internet, outbound to the internet, and from region to region. In addition, Azure currently does not provide layer 7 (L7) protection. So having a good L7 defense strategy in place is recommended.



