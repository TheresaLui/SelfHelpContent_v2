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
            articleId="dc85e56c-1a1a-40c1-8128-b039201094e6"
            ownershipId="Centennial_CloudNet_LoadBalancer" />

# DDoS Protection Basic Customers

1. The first step in a DDoS Protection Basic "I'm under Attack" SR is to ensure the customer is over 10k pps. If the attack is above 10k pps, the next step is to have the customer enable DDoS Protection Standard on the affected vnet(s). Without this in place, the benefits of Azure DDoS Protection will *not* be applied in any scenario.
2. Next, you can get a view of the current state of their networking using the dashboards outlined in the [Log Sources for DDoS Protection](https://supportability.visualstudio.com/AzureNetworking/_wiki/wikis/Wiki/209767/Log-Sources-for-DDoS-Protection) wiki. Having this information handy when you post to Microsoft Teams or in a CRI is critical for the DDoS team to quickly take action and mitigate a customer's impact.
3. Identify if the attack is a Layer 7 Attack. Please be aware that customers may feel that they are currently undergoing a DDoS attack, when in fact their resource simply cannot keep up with the number of incoming requests (for example: a "small" SKU AppGW cannot handle too many web requests before its CPU is pegged to 100%). For more information about these L7 attacks, including how to mitigate and protect against them, please see [TSG: Layer 7 DDoS Attack](https://supportability.visualstudio.com/AzureNetworking/_wiki/wikis/Wiki/326854).
4. If the attack is NOT a Layer 7 Attack, and is instead a Layer 3 / Layer 4 Attack, continue furtherc. Azure DDoS Protection Standard currently provides protection against layer 3 (L3) and layer 4 (L4) DDoS attacks, which include TCP SYN, New Connections, UDP/ICMP/TCP floods. All Azure endpoint VIPs (/32) are guarded at platform safe thresholds. The protection extends to traffic flows inbound from the internet, outbound to the internet, and from region to region.
5. Normally, once you enable DDoS Protection Standard, a customer has to wait ~2 weeks to be fully learned and protected from DDoS attacks. However, in an "I'm Under Attack" scenario, the Azure PG will set artificially low thresholds to quickly mitigate the customer impact. 
6. **There is no need to wait 2 weeks for mitigation**. Once DDoS Standard is enabled, please post in the [Microsoft Teams DDoS Channel](https://teams.microsoft.com/l/channel/19%3a9e0120d9ea8b479e8c603012f1b15e8f%40thread.skype/Azure%2520DDoS?groupId=c3e00ac7-3f76-4350-ba3b-e335a6bbbe21&tenantId=72f988bf-86f1-41af-91ab-2d7cd011db47) to discuss the issue with a TA/PG for further action and approval for CRI using template <https://aka.ms/CRI-DDOSATTACK>. Remember, ANP always requires TA/PG approval for CRIs.
