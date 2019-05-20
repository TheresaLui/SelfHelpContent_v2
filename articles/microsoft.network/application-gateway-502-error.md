<properties 
    pageTitle="I'm encountering Bad Gateway Error (502)"
    description="Bad Gateway Error (502)"
    infoBubbleText="Common solution article for instructions on how to troubleshoot Bad Gateway errors with Application Gateway."
    service="microsoft.network"
    resource="applicationgateways"
    authors="abshamsft"
    ms.author="absha"
    selfHelpType="resource"
    articleId="application-gateway-502-error"
    diagnosticScenario="ApplicationGateway502BadGatewayError"
    supportTopicIds="32573483"
    cloudEnvironments="public"
 />

# Bad Gateway Error (502)

## **Recommended Steps**

You can see a Bad Gateway Error (502) when there is an issue with the backend application. You can identify this by bypassing the Application Gateway to directly access the backend. If the backend server still returns the same 502 error, then the issue is with the backend and not the Application Gateway.

If it is verified that the backend is healthy, then perform the steps in links below to troubleshoot the issue.

## **Recommended Documents**

The bad gateway error (502) can happen due to one or more of the following issues:

- [NSG, UDR or Custom DNS is blocking access to backend pool members](https://docs.microsoft.com/azure/application-gateway/application-gateway-troubleshooting-502#network-security-group-user-defined-route-or-custom-dns-issue). 
- [Back-end VMs or instances of virtual machine scale set are not responding to the default health probe.](https://docs.microsoft.com/azure/application-gateway/application-gateway-troubleshooting-502#problems-with-default-health-probe)
- [Invalid or improper configuration of custom health probes.](https://docs.microsoft.com/azure/application-gateway/application-gateway-troubleshooting-502#problems-with-custom-health-probe)
- [Request time-out or connectivity issues with user requests.](https://docs.microsoft.com/azure/application-gateway/application-gateway-troubleshooting-502#request-time-out)
- [Empty backend pool](https://docs.microsoft.com/azure/application-gateway/application-gateway-troubleshooting-502#empty-backendaddresspool).
- [Unhealthy instances in the backend pool](https://docs.microsoft.com/azure/application-gateway/application-gateway-troubleshooting-502#unhealthy-instances-in-backendaddresspool).
