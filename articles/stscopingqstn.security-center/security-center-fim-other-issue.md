<properties
    pageTitle="Azure Security Center File Integrity monitor - FIM other issue Common Solutions"
    description="Azure Security Center File Integrity monitor - FIM other issue Common Solutions"
    authors="genlin"
    ms.author="jaserano"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32636875"
    resourceTags=""
    productPesIds="15947"
    cloudEnvironments="public, fairfax, usnat, ussec"
    articleId="a15f057d-9001-9991-a98a-dfaf3843dc2f"
	ownershipId="Azure_Security_Security_Center"
/>

# Azure Security Center File Integrity monitor - FIM other issue

## **Recommended Steps**

File Integrity monitor uses the Azure Change Tracking solution to track and identify changes in your environment. When File Integrity Monitoring is enabled, a Change Tracking resource (Log Analytics workspace) is created in your subscription. If you remove this Change Tracking resource, File Integrity Monitoring feature will be disabled.

To resolve the configuration failure, you need to open the relevant Log Analytics workspace, and check the **Solution** section to see if the following two solutions are presented:

- Security
- Change tracking

If one of these two solutions are not enable on the workspace solution list, go to **Security Center - File Integrity Monitoring** and click **Upgrade** and **Enable**.

**Tips for troubleshooting**

- File Integrity monitor works only on Azure VMs and on-premises VMs.
- The server that enables File Integrity monitoring must be monitored by Azure security center and the Azure Log Analytics agent must to be healthy.
- Azure security center needs to be on standard mode on the subscription level, and every User workspace that the end-user wants to use should also be in standard (security solution be should install on it).
- File Integrity monitor does not work with PaaS services.
- The File Integrity monitor UI in Azure portal only shows the last 100 changes. You should always run log analytics query to check if the changes appear in the user workspace.

## **Recommended Documents**

- [File Integrity Monitoring in Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-file-integrity-monitoring)
- [File Integrity Monitoring Limitations](https://docs.microsoft.com/azure/automation/automation-change-tracking#change-tracking-data-collection-details)
- [Azure Security Center FAQ](https://docs.microsoft.com/azure/security-center/security-center-faq)

**Troubleshooting**

- [Azure Security Center Troubleshooting Guide](https://docs.microsoft.com/azure/security-center/security-center-troubleshooting-guide)

**How-To and Advisory Information**

- [Azure Security Center Pricing Tiers](https://docs.microsoft.com/azure/security-center/security-center-pricing)
- [Azure Security Center Readiness Roadmap](https://docs.microsoft.com/azure/security-center/security-center-readiness-roadmap)
- [Permissions in Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-permissions)
- [Azure Security Center REST API](https://docs.microsoft.com/rest/api/securitycenter/)
- [Check out our latest Azure Security Center updates](https://azure.microsoft.com/updates/?product=security-center)
