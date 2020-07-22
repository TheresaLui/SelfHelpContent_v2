<properties
    pageTitle="Restrict outgoing FQDN traffic using application rule collections"
    description="Restrict outgoing FQDN traffic using application rule collections"
    service="microsoft.network"
    resource="azurefirewalls"
    authors="v-miegge"
    ms.author="Mario.Liu"
    selfHelpType="generic"
    supportTopicIds="32745466"
    resourceTags=""
    productPesIds="16556"
    ownershipId="CloudNet_AzureFirewall"
    cloudEnvironments="public,fairfax,blackforest,mooncake,usnat,ussec"
    articleId="da5afa70-933b-4e25-bb3a-41953f8256ce"
/>

# Restrict outgoing FQDN traffic using application rule collections

You can limit outbound HTTP/S traffic or Azure SQL traffic (preview) to a specified list of fully qualified domain names (FQDN) including wild cards. This feature does not require TLS termination.

## **Recommended Documents**

- Use the Azure Portal to [configure application rule](https://docs.microsoft.com/azure/firewall/tutorial-firewall-deploy-portal#configure-an-application-rule).
- Use an [FQDN tag](https://docs.microsoft.com/azure/firewall/fqdn-tags) in application rules to allow application centric (like AKS, ASE, SQL) outbound traffic through your firewall.
- Configure NAT rules, network rules, and applications rules on Azure Firewall. Rule collections are processed according to the rule type in priority order. For more information, learn about [rule collection priority](https://docs.microsoft.com/azure/firewall/rule-processing).
- Learn more about [Azure Firewall](https://docs.microsoft.com/azure/firewall/overview), [Firewall FAQs](https://docs.microsoft.com/azure/firewall/firewall-faq) and [known issues](https://docs.microsoft.com/azure/firewall/overview#known-issues).
