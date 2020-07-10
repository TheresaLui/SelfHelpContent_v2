<properties
    pageTitle="Connectivity issues to the protected resource"
    description="Connectivity issues to the protected resource"
    service="microsoft.network"
    resource="ddosProtectionPlans"
    authors="radwiv"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32605609"
    resourceTags=""
    productPesIds="16355"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="b6d3a479-bf9f-413e-9a0c-163af5cb92f5"
	ownershipId="CloudNet_AzureDDoSProtection"
/>
# Connectivity issues to the protected resource
## **Recommended steps**
If the incoming traffic is higher than [DDoS trigger thresholds](https://docs.microsoft.com/azure/virtual-network/ddos-protection-manage-portal#use-ddos-protection-telemetry), DDoS will initiate the mitigation.<br>
If the incoming traffic is lower than DDoS trigger thresholds, then you can follow below steps to address most common connectivity issues: <br>
1.	Check that Backend resource pool is online. <br>
2.	Review the application logs to troubleshoot potential connectivity problems.
