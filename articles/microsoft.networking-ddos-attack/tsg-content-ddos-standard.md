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
            articleId="d3a17175-5df7-486c-bece-9a5166fe9eec"
            ownershipId="Centennial_CloudNet_LoadBalancer" />

# DDoS Protection Standard Customers & ARR

1. If the customer is using DDoS Protection Standard, you can get a view of the current state of their networking using the CNS dashboards outlined in the [Log Sources for DDoS Protection](https://supportability.visualstudio.com/AzureNetworking/_wiki/wikis/Wiki/209767/Log-Sources-for-DDoS-Protection) wiki. Having this information handy when you post to Microsoft Teams or in a CRI is critical for the DDoS team to quickly take action and mitigate a customer's impact.
2. A new DDOS support topic called "Under Attack" is available as of 2018-09-21. This provides a 15min support response time for "Under Attack" scenarios. These calls will route to the ARR team instead of the Azure Networking POD (ANP). ARR teams are expected to engage the Dev team via a CRI immediately. ARR teams are also expected to proactively reach out to customers acknowledging assignment and direct engagement is available. ARR teams assigned this case are empowered to reach out to the DDoS Protection Service Dev team (i.e., the current on-call)
3. As with ARR customers, if we have a customer with DDoS Standard, and they are under DDoS attack, please use this template for the CRI, **with TA approval in [Microsoft Teams](https://teams.microsoft.com/l/channel/19%3a9e0120d9ea8b479e8c603012f1b15e8f%40thread.skype/Azure%2520DDoS?groupId=c3e00ac7-3f76-4350-ba3b-e335a6bbbe21&tenantId=72f988bf-86f1-41af-91ab-2d7cd011db47)**: 
4. If ASC doesn't have the proper template available, use this shortlink: [DDOS CRI Template](https://aka.ms/CRI-DDOSATTACK)
