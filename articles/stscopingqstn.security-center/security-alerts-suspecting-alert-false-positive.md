<properties
    pageTitle="Security Alerts - Suspecting alert false positive Common Solutions"
    description="Security Alerts - Suspecting alert false positive Common Solutions"
    service=""
    resource=""
    authors="jaserano, v-miegge"
    ms.author="jaserano"
    authorAlias="jaserano"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32636915"
    resourceTags=""
    productPesIds="15947"
    cloudEnvironments="public, fairfax, usnat, ussec"
    articleId="05bf673e-e051-4d97-8a7f-bb3bb7aee044"
	ownershipId="Azure_Security_Security_Center"
/>

# Security Alerts - Suspecting alert false positive Common Solutions

## Alerts types

* Virtual Machine Behavioral Analysis (VMBA)<br>
* Network Analysis<br>
* SQL Database and SQL Data Warehouse Analysis<br>
* Contextual Information

Depending on the alert types, customers can gather the necessary information to investigate the alert by using the following resources:

* Security logs in the Virtual Machine (VM) event viewer in Windows<br>
* AuditD in Linux<br>
* The [Azure activity logs](https://docs.microsoft.com/azure/azure-monitor/platform/activity-logs-overview), and the [enable diagnostic logs](https://docs.microsoft.com/azure/azure-monitor/platform/diagnostic-logs-overview#how-to-enable-collection-of-diagnostic-logs) on the attack resource.

For some alerts we also have a [confidence score](https://docs.microsoft.com/azure/security-center/security-center-confidence-score). The confidence score in **Security Center** can help your team triage and prioritize alerts. **Security Center** automatically applies industry best practices, intelligent algorithms, and processes used by analysts to determine whether a threat is legitimate, and provides meaningful insights in the form of a confidence score.

Customers can share feedback for the alert description and relevance. Navigate to the alert itself, select the **Was This Useful** button, select the reason, and then enter a comment to explain which explains the feedback. We consistently monitor this feedback channel to improve our alerts.

## **Recommended Documents**

* [Managing and responding to security alerts in Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-managing-and-responding-alerts)<br>
* [Understanding security alerts in Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-alerts-type)<br>
* [Tutorial: Respond to security incidents](https://docs.microsoft.com/azure/security-center/tutorial-security-incident)<br>
* [Alerts Validation in Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-alert-validation)<br>
* [Email Notifications in Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-provide-security-contact-details)<br>
* [Handling Security Incidents in Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-incident)<br>
* [Alert confidence score](https://docs.microsoft.com/azure/security-center/security-center-confidence-score)<br>
* [Investigate Incidents and Alerts in Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-investigation)<br>
* [Azure Security Center detection capabilities](https://docs.microsoft.com/azure/security-center/security-center-detection-capabilities)

## Troubleshooting

* [ASC Troubleshooting Guide](https://docs.microsoft.com/azure/security-center/security-center-troubleshooting-guide)

## FAQ

* [ASC FAQ](https://docs.microsoft.com/azure/security-center/security-center-faq)