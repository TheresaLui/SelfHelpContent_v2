<properties
    pageTitle="containers-overview"
    description="Containers Monitoring Overview (Does not include Security, Update Management, and Linux Agent)"
    service="microsoft.operationalinsights"
    resource="operationalinsightsaccounts"
    authors="keikhara"
    ms.author="keikhara"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="32745413"
    resourceTags=""
    productPesIds="15725"
    cloudEnvironments="public, Blackforest, Fairfax, usnat, ussec"
    articleId="70e04d6f-8ef4-4ef9-84cc-63a1355d02f0"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# Container Monitoring Overview

There are two container monitoring tools available: **Azure Monitor for Container** (Container Insights), and **Container Monitoring Solution**. For those who have Azure Kubernetes Service or Azure Kubernetes Service Engine (Linux only), they should be using Azure Monitor for Containers. For everything else, please use Container Monitoring Solution. 

Container Monitoring does not include Update Management, Security Management, AKS Azure Monitor metrics, and Linux Agent. Please go to the appropriate selection for those. 

## **Recommended Documents**

* [Container Monitoring Solution](https://docs.microsoft.com/azure/azure-monitor/insights/containers)
* [Azure Monitor for containers (Container Insights)](https://docs.microsoft.com/azure/azure-monitor/insights/container-insights-overview)

### Troubleshooting and FAQ

* [Azure Monitor for containers FAQ](https://docs.microsoft.com/azure/azure-monitor/insights/container-insights-faq)
* [Azure Monitor for containers Troubleshoot](https://docs.microsoft.com/azure/azure-monitor/insights/container-insights-troubleshoot)

### Release Notes for Agent

* [Azure Monitor for containers Agent Release Notes](https://github.com/Microsoft/docker-provider/tree/ci_feature_prod#release-history)
* [Container Monitoring Solution Agent Release Notes](https://github.com/Microsoft/Docker-Provider/tree/master#release-history)

### Known Issues

AKS [Azure Monitor metrics](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-charts) does not match the actual counts and performance of AKS cluster. To open a case related to Azure Monitor metrics for AKS, please go to the support portal and select *Issue Type = Technical* and *Service=Metrics*. If you need performance information on your AKS cluster, Azure Monitor for containers can also provide metric for AKS. 
