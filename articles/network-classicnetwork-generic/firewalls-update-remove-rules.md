<properties
    pageTitle="Issues with updating or removing Azure Firewall rules"
    description="Issues with updating or removing Azure Firewall rules"
    service="microsoft.network"
    resource="azurefirewalls"
    authors="v-miegge"
    ms.author="Mario.Liu"
    selfHelpType="generic"
    supportTopicIds="32745463"
    resourceTags=""
    productPesIds="16556"
    ownershipId="CloudNet_AzureFirewall"
    cloudEnvironments="public,fairfax,blackforest,mooncake,usnat,ussec"
    articleId="4b1fd0c6-5bb4-4243-8483-142ad6d37292"
/>

# Issues with updating or removing Azure Firewall rules

Whenever a configuration change is applied, Azure Firewall attempts to update all its underlying backend instances. In rare cases, one of these backend instances may fail to update with the new configuration and the update process stops with a failed provisioning state. Your Azure Firewall may still be operational, but the applied configuration may be in an inconsistent state, where some instances have the previous configuration where others have the updated rule set.

## **Recommended Steps**

1. Try updating your configuration one more time until the operation succeeds, and your Firewall is in a **Succeeded** provisioning state
1. Azure Firewall must have direct Internet connectivity. If your **Azure Firewall Subnet** learns a default route to your on-premises network via Border Gateway Patrol (BGP), you must override this with a 0.0.0.0/0 UDR with the **NextHopType** value set as **Internet** to maintain direct Internet connectivity.
1. Check whether IPv6 is used in DNAT or Network rules. This is currently not supported and can cause control plane operations to fail.
1. Reach out to support if the problem continues

## **Recommended Documents**

- Learn more about [Azure Firewall](https://docs.microsoft.com/azure/firewall/overview), [Firewall FAQs](https://docs.microsoft.com/azure/firewall/firewall-faq) and [known issues](https://docs.microsoft.com/azure/firewall/overview#known-issues)
