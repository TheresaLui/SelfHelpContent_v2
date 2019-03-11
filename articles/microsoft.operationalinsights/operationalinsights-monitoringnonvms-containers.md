<properties
    pageTitle="containers-overview"
    description="Containers Monitoring Overview (Does not include Security, Update Management, and Linux Agent"
    service="microsoft.operationalinsights"
    resource="operationalinsightsaccounts"
    authors="adoylemsft"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="32536629"
    resourceTags=""
    productPesIds="15725"
    cloudEnvironments="public, Blackforest, Fairfax"
	articleId="70e04d6f-8ef4-4ef9-84cc-63a1355d02f0"
/>

# Container Monitoring Overview
There are two container monitoring tools out there: Azure Monitor for containers (Container Insights) and Container Monitoring Solution. For those who have Azure Kubernetes Service or Azure Kubernetes Service Enginei(Linux only), they should be using Azure Monitor for containers. For everything else, please use Container Monitoring Solution. 

<<<<<<< HEAD
Container Monitoring does not include Update Management, Security Management, AKS Azure Monitor metrics, and Linux Agent. Please go to the appropriate selection for those. 

=======
>>>>>>> 1d9c04161bfc7d98d9f9e2b46c096e548e9b8945
## Documentations
- [Container Monitoring Solution](https://docs.microsoft.com/en-us/azure/azure-monitor/insights/containers)
- [Azure Monitor for containers (Container Insights)](https://docs.microsoft.com/en-us/azure/azure-monitor/insights/container-insights-overview)

## Troubleshooting and FAQ
- [Azure Monitor for containers FAQ](https://docs.microsoft.com/en-us/azure/azure-monitor/insights/container-insights-faq)
- [Azure Monitor for containers Troubleshoot](https://docs.microsoft.com/en-us/azure/azure-monitor/insights/container-insights-troubleshoot)

## Release Note for Agent
- [Azure Monitor for containers Agent Release Note](https://github.com/Microsoft/docker-provider/tree/ci_feature_prod#release-history)
- [Container Monitoring Solutioni Agent Release Note](https://github.com/Microsoft/Docker-Provider/tree/master#release-history)

## Known Issues
<<<<<<< HEAD
- AKS [Azure Monitor metrics](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/metrics-charts) does not match the actual counts and performance of AKS clsuster. To raise issues, please go to xxxxx to raise the issue. For AKS metrics, please Azure Monitor for containers.
=======
- AKS Azure Monitor metrics does not match the actual counts and performance of AKS clsuster. To raise a case, please go to xxxxx to raise the issue. For AKS metrics, please use Azure Monitor for containers.
>>>>>>> 1d9c04161bfc7d98d9f9e2b46c096e548e9b8945
