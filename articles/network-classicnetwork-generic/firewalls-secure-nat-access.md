<properties
    pageTitle="Secure NAT access to Azure Virtual Machines from Internet"
    description="Secure NAT access to Azure Virtual Machines from Internet"
    service="microsoft.network"
    resource="azurefirewalls"
    authors="v-miegge"
    ms.author="Mario.Liu"
    selfHelpType="generic"
    supportTopicIds="32745469"
    resourceTags=""
    productPesIds="16556"
    ownershipId="CloudNet_AzureFirewall"
    cloudEnvironments="public,fairfax,blackforest,mooncake,usnat,ussec"
    articleId="8f3cc419-b7b7-4a25-b29d-d6f855aaf9df"
/>

# Secure NAT access to Azure Virtual Machines from Internet

You can configure Azure Firewall Destination Network Address Translation (DNAT) to translate and filter inbound Internet traffic to your subnets.

When you configure DNAT, the NAT rule collection action is set to DNAT. Each rule in the NAT rule collection can then be used to translate your firewall public IP and port to a private IP and port.

## **Recommended Documents**

- Use the [step by step guide](https://docs.microsoft.com/azure/firewall/tutorial-firewall-dnat) to Filter inbound Internet traffic with Azure Firewall DNAT using the Azure portal.
- Learn more about [Azure Firewall](https://docs.microsoft.com/azure/firewall/overview), [Firewall FAQs](https://docs.microsoft.com/azure/firewall/firewall-faq) and [known issues](https://docs.microsoft.com/azure/firewall/overview#known-issues).
