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


First, determine if the customer is using DDoS Protection Standard SKU or not. This is very [easy to do](https://supportability.visualstudio.com/AzureNetworking/_wiki/wikis/Wiki/300601/TSG-Determine-Customer's-DDoS-SKU). It can be located in ASC as a resourceType for quick identification. If you see Microsoft.Network/ddosProtectionPlans listed in ASC, it's DDoS Protection Standard customer.

**Important**: If the customer has an ARR support contract then the case will stay with ARR regardless of DDoS Basic or Standard.  Please check this before sending to the PODs.

**DDoS Protection Basic Customers**

1. The first step in a DDoS Protection Basic "I'm under Attack" SR is to ensure the customer is over 10k pps. If the attack is above 10k pps, the next step is to have the customer enable DDoS Protection Standard on the affected vnet(s). Without this in place, the benefits of Azure DDoS Protection will *not* be applied in any scenario.
2. Normally, once you enable DDoS Protection Standard, a customer has to wait ~2 weeks to be fully learned and protected from DDoS attacks. However, in an "I'm Under Attack" scenario, the Azure PG will set artificially low thresholds to quickly mitigate the customer impact. 
3. **There is no need to wait 2 weeks for mitigation**. Once DDoS Standard is enabled, please post in the [Microsoft Teams DDoS Channel](https://teams.microsoft.com/l/channel/19%3a9e0120d9ea8b479e8c603012f1b15e8f%40thread.skype/Azure%2520DDoS?groupId=c3e00ac7-3f76-4350-ba3b-e335a6bbbe21&tenantId=72f988bf-86f1-41af-91ab-2d7cd011db47) to discuss the issue with a TA/PG for further action and approval for CRI using template <https://aka.ms/CRI-DDOSATTACK>. Remember, ANP always requires TA/PG approval for CRIs.

**DDoS Protection Standard Customers & ARR**


1. If the customer is using DDoS Protection Standard, you can get a view of the current state of their networking using the CNS dashboards outlined in the [Log Sources for DDoS Protection](https://supportability.visualstudio.com/AzureNetworking/_wiki/wikis/Wiki/209767/Log-Sources-for-DDoS-Protection) wiki. Having this information handy when you post to Microsoft Teams or in a CRI is critical for the DDoS team to quickly take action and mitigate a customer's impact.
2. A new DDOS support topic called "Under Attack" is available as of 2018-09-21. This provides a 15min support response time for "Under Attack" scenarios. These calls will route to the ARR team instead of the Azure Networking POD (ANP). ARR teams are expected to engage the Dev team via a CRI immediately. ARR teams are also expected to proactively reach out to customers acknowledging assignment and direct engagement is available. ARR teams assigned this case are empowered to reach out to the DDoS Protection Service Dev team (i.e., the current on-call)
3. As with ARR customers, if we have a customer with DDoS Standard, and they are under DDoS attack, please use this template for the CRI, **with TA approval in [Microsoft Teams](https://teams.microsoft.com/l/channel/19%3a9e0120d9ea8b479e8c603012f1b15e8f%40thread.skype/Azure%2520DDoS?groupId=c3e00ac7-3f76-4350-ba3b-e335a6bbbe21&tenantId=72f988bf-86f1-41af-91ab-2d7cd011db47)**: 
4. If ASC doesn't have the proper template available, use this shortlink: https://aka.ms/CRI-DDOSATTACK 


**NOTE:** Anything under 10k packets/sec is NOT considered a DDoS by Microsoft's definition. Customers will need to scale their resources to handle this, as DDoS Protection Standard cannot protect below this figure.

**NOTE:** Azure also currently provides protection against layer 3 (L3) and layer 4 (L4) DDoS attacks, which include TCP SYN, New Connections, UDP/ICMP/TCP floods. All Azure endpoint VIPs (/32) are guarded at platform safe thresholds. The protection extends to traffic flows inbound from the internet, outbound to the internet, and from region to region. In addition, Azure currently does not provide layer 7 (L7) protection. So having a good L7 defense strategy in place is recommended.



