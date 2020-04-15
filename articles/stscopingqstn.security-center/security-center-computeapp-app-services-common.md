<properties
    pageTitle="App Services Common Solutions"
    description="App Services Common Solutions"
    service=""
    resource=""
    authors="TobyTu"
    ms.author="jaserano"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32636863"
    resourceTags=""
    productPesIds="15947"
    cloudEnvironments="public, fairfax, usnat, ussec"
    articleId="a15r058d-1uj6-4b97-a98a-dfaf3843dc2f"
	ownershipId="Azure_Security_Security_Center"
/>

# App Services Common Solutions

Azure Security Center protects the management interface and the VM instance in which your App Service is running. It also monitors requests and responses sent to and from your apps running in App Service, the integration is completely transparent.

## **Recommended Steps**

**Tips for troubleshooting**

- To monitor and secure your App Service, you have to have an App Service plan that is associated with dedicated machines. These plans are: Basic, Standard, Premium, Isolated, or Linux. Azure Security Center does not support the Free, Shared, or Consumption plans. For more information, see [App Service Plans](https://docs.microsoft.com/azure/app-service/overview-hosting-plans)
- To be able to received security alerts on web apps, your Azure Security Center pricing plan should be standard on App Service Bundle
- Azure Security Center also send recommendation on your web apps in Azure to help you improve your security posture. This recommendation is part of the Free tier of the product and refresh every 12 hours

## **Recommended Documents**

- [Protect App Service with Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-app-services)

- [App Service with Azure Security Center](https://azure.microsoft.com/blog/azure-security-center-can-identify-attacks-targeting-azure-app-service-applications/)

**Troubleshooting**

- [Azure Security Center Troubleshooting Guide](https://docs.microsoft.com/azure/security-center/security-center-troubleshooting-guide)

**FAQ**

- [Azure Security Center FAQ](https://docs.microsoft.com/azure/security-center/security-center-faq)
