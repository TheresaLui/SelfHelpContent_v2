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
2. Normally, once you enable DDoS Protection Standard, a customer has to wait ~2 weeks to be fully learned and protected from DDoS attacks. However, in an "I'm Under Attack" scenario, the Azure PG will set artificially low thresholds to quickly mitigate the customer impact. 
3. **There is no need to wait 2 weeks for mitigation**. Once DDoS Standard is enabled, please post in the [Microsoft Teams DDoS Channel](https://teams.microsoft.com/l/channel/19%3a9e0120d9ea8b479e8c603012f1b15e8f%40thread.skype/Azure%2520DDoS?groupId=c3e00ac7-3f76-4350-ba3b-e335a6bbbe21&tenantId=72f988bf-86f1-41af-91ab-2d7cd011db47) to discuss the issue with a TA/PG for further action and approval for CRI using template <https://aka.ms/CRI-DDOSATTACK>. Remember, ANP always requires TA/PG approval for CRIs.
