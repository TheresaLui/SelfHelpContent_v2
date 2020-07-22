<properties
    pageTitle="Troubleshoot SNAT port utilization issue"
    description="Troubleshoot SNAT port utilization issue"
    service="microsoft.network"
    resource="azurefirewalls"
    authors="v-miegge"
    ms.author="Mario.Liu"
    selfHelpType="generic"
    supportTopicIds="32745454, 32745475"
    resourceTags=""
    productPesIds="16556"
    ownershipId="CloudNet_AzureFirewall"
    cloudEnvironments="public,fairfax,blackforest,mooncake,usnat,ussec"
    articleId="7a47baa4-4e3a-47c4-b94b-999baa852023"
/>

# Troubleshoot SNAT port utilization issue

Azure Firewall health state metric indicates the health of the firewall based on (static network address translation) SNAT port availability. This metric has two dimensions:

- Status: Possible values are Healthy, Degraded, Unhealthy.
- Reason: Indicate the reason for the corresponding status of the firewall.

If SNAT ports are used greater than 95%, they are considered exhausted and the health is 50% with `status=Degraded` and `reason=SNAT port`. The firewall keeps processing traffic and existing connections are not affected. However, new connections may not be established intermittently.

If SNAT ports are used less than 95%, then firewall is considered healthy and health is shown as 100%.

If no SNAT ports usage is reported, health is shown as 0%.

**SNAT port utilization metrics** indicate the percentage of SNAT ports that have been used by the firewall.

When you add more public IP addresses to your firewall, more SNAT ports are available, reducing the SNAT ports utilization. Additionally, when the firewall scales out for different reasons (for example, CPU or throughput) additional SNAT ports also become available. So a given percentage of SNAT ports utilization may go down without you adding any public IP addresses, because the service scaled out. You can directly control the number of public IP addresses available to increase the ports available on your firewall. But you can't directly control firewall scaling. SNAT ports are currently added only for the first five public IP addresses.

## **Recommended Documents**

- Learn how to [monitor Azure Firewall logs and metrics](https://docs.microsoft.com/azure/firewall/tutorial-diagnostics).
- Learn more about [Metrics in Azure Monitor](https://docs.microsoft.com/azure/azure-monitor/platform/data-platform-metrics).
- Learn more about [Azure Firewall](https://docs.microsoft.com/azure/firewall/overview), [Firewall FAQs](https://docs.microsoft.com/azure/firewall/firewall-faq) and [known issues](https://docs.microsoft.com/azure/firewall/overview#known-issues).
