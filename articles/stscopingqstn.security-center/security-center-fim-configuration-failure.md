<properties
    pageTitle="Azure Security Center File Integrity monitor - FIM Configuration failure"
    description="Azure Security Center File Integrity monitor - FIM Configuration failure"
    authors="genlin"
    ms.author="jaserano"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32636843,32636876"
    resourceTags=""
    productPesIds="15947"
    cloudEnvironments="public, fairfax, usnat, ussec"
    articleId="a15f057d-9001-2012-a98a-dfaf3843dc2f"
	ownershipId="Azure_Security_Security_Center"
/>

#  Azure Security Center File Integrity monitor Configuration failure

## **Recommended Steps**

To resolve the configuration failure, you have to open the relevant Log Analytics workspace, and check the **Solution** section to see whether the following solutions are presented:

- Security
- Change tracking

If one of these two solutions are not enabled on the workspace solution list, go to **Security Center - File Integrity Monitoring**, and press **Enable** or **Upgrade**.

**Tips for troubleshooting**

- File Integrity monitor works only on Azure virtual machines (VMs) and on-premises VMs
- The server must be monitored by Azure Security Center, and the Azure Log Analytics agent must be shown as healthy
- Azure security center has to be on Standard mode on the subscription level, and every User workspace that the user wants should also be in Standard mode (that is, a security solution be should installed on it)
- File Integrity Monitor does not work for the PaaS services
- The File Integrity Monitor UI in Azure portal shows only the last 100 changes. You should always run a log analytics query to check whether the changes appear in the user workspace.

## **Recommended Documents**

- [File Integrity Monitoring in Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-file-integrity-monitoring)
- [File Integrity Monitoring Limitations](https://docs.microsoft.com/azure/automation/automation-change-tracking#change-tracking-data-collection-details)
- [Azure Security Center FAQ](https://docs.microsoft.com/azure/security-center/security-center-faq)

**Troubleshooting**

- [Azure Security Center Troubleshooting Guide](https://docs.microsoft.com/azure/security-center/security-center-troubleshooting-guide)

**How to and advisory information**

- [Azure Security Center Pricing Tiers](https://docs.microsoft.com/azure/security-center/security-center-pricing)
- [Azure Security Center Readiness Roadmap](https://docs.microsoft.com/azure/security-center/security-center-readiness-roadmap)
- [Permissions in Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-permissions)
- [Azure Security Center REST API](https://docs.microsoft.com/rest/api/securitycenter/)
- [Check out our latest Azure Security Center updates](https://azure.microsoft.com/updates/?product=security-center)
