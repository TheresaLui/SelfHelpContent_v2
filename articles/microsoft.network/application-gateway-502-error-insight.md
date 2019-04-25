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
    cloudEnvironments="public"
 />

# Bad Gateway Error (502)

We ran several diagnostic checks on your resource **<!--$ImpactedResource-->[ImpactedResource]<!--/$ImpactedResource-->**. The status of the each diagnostic check is mentioned below. Please troubleshoot the issues which have been flagged as 'failed'.

## **Diagnostic checks executed**

* Check for <!--$BackendAddressPoolEmptyDiaplayname-->[BackendAddressPoolEmptyDiaplayname]<!--/$BackendAddressPoolEmptyDiaplayname--> - <!--$BackendAddressPoolEmptyCheckStatus-->[BackendAddressPoolEmptyCheckStatus]<!--/$BackendAddressPoolEmptyCheckStatus-->

    * [Troubleshoot](https://docs.microsoft.com/azure/application-gateway/application-gateway-troubleshooting-502#empty-backendaddresspool) <br>

* Check for <!--$DegradedBackendServerHealthDiaplayname-->[DegradedBackendServerHealthDiaplayname]<!--/$DegradedBackendServerHealthDiaplayname--> - <!--$DegradedBackendServerHealthCheckStatus-->[DegradedBackendServerHealthCheckStatus]<!--/$DegradedBackendServerHealthCheckStatus-->

    * [Troubleshoot](https://docs.microsoft.com/azure/application-gateway/application-gateway-troubleshooting-502#unhealthy-instances-in-backendaddresspool) <br>

* Check for  <!--$BasicListenerHasHigherPriorityRuleThanMultiSiteDiaplayname-->[BasicListenerHasHigherPriorityRuleThanMultiSiteDiaplayname]<!--/$BasicListenerHasHigherPriorityRuleThanMultiSiteDiaplayname--> - <!--$BasicListenerHasHigherPriorityRuleThanMultiSiteCheckStatus-->[BasicListenerHasHigherPriorityRuleThanMultiSiteCheckStatus]<!--/$BasicListenerHasHigherPriorityRuleThanMultiSiteCheckStatus-->

    * [Troubleshoot](https://docs.microsoft.com/azure/application-gateway/configuration-overview#order-of-processing-listeners)

## **Recommended Steps**

If none of diagnostic checks above resolve your issue, the following are other issues which can result in Bad
Gateway Error (502):

- [NSG, UDR or Custom DNS is blocking access to backend pool members](https://docs.microsoft.com/azure/application-gateway/application-gateway-troubleshooting-502#network-security-group-user-defined-route-or-custom-dns-issue)
- [Back-end VMs or instances of virtual machine scale set are not responding to the default health probe](https://docs.microsoft.com/azure/application-gateway/application-gateway-troubleshooting-502#problems-with-default-health-probe)
- [Invalid or improper configuration of custom health probes](https://docs.microsoft.com/azure/application-gateway/application-gateway-troubleshooting-502#problems-with-custom-health-probe)
- [Request time-out or connectivity issues with user requests](https://docs.microsoft.com/azure/application-gateway/application-gateway-troubleshooting-502#request-time-out)
