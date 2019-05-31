<properties 
    pageTitle="I'm encountering Bad Gateway Error (502)"
    description="Bad Gateway Error (502)"
    infoBubbleText="Some suggestions have been found to help solve your Bad Gateway Error (502) issue quicker."
    service="microsoft.network"
    resource="applicationgateways"
    authors="abshamsft"
    ms.author="absha"
    selfHelpType="diagnostics"
    articleId="application-gateway-502-error-insight"
    diagnosticScenario="ApplicationGateway502BadGatewayError"
    supportTopicIds="32573483"
	productPesIds="15922"
    cloudEnvironments="public"
 />

# Bad Gateway Error (502)

We ran several diagnostics on your resource **<!--$ImpactedResource-->[ImpactedResource]<!--/$ImpactedResource-->** and have found the below issues because of which you are encountering Bad Gateway Error (502).

## **Issues identified**

 <!--$failedCheckList-->[failedChecklist]<!--/$failedCheckList-->

## **Recommended Steps**

Use the instructions below to troubleshoot the issues identified by the diagnostics:

- [Unhealthy instances in backend address pool](https://docs.microsoft.com/azure/application-gateway/application-gateway-troubleshooting-502#unhealthy-instances-in-backendaddresspool) 
- [Empty backend address pool](https://docs.microsoft.com/azure/application-gateway/application-gateway-troubleshooting-502#empty-backendaddresspool)
- [Incorrect order of processing listeners](https://docs.microsoft.com/azure/application-gateway/configuration-overview#order-of-processing-listeners)

The following are other issues which cannot be identified by the diagnostics but can result in Bad Gateway Error (502):

- [NSG, UDR or Custom DNS is blocking access to backend pool members](https://docs.microsoft.com/azure/application-gateway/application-gateway-troubleshooting-502#network-security-group-user-defined-route-or-custom-dns-issue)
- [Back-end VMs or instances of virtual machine scale set are not responding to the default health probe](https://docs.microsoft.com/azure/application-gateway/application-gateway-troubleshooting-502#problems-with-default-health-probe)
- [Invalid or improper configuration of custom health probes](https://docs.microsoft.com/azure/application-gateway/application-gateway-troubleshooting-502#problems-with-custom-health-probe)
- [Request time-out or connectivity issues with user requests](https://docs.microsoft.com/azure/application-gateway/application-gateway-troubleshooting-502#request-time-out)
