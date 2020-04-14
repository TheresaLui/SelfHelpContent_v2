<properties
    pageTitle="Security Alerts - No alerts generated Common Solutions"
    description="Security Alerts - No alerts generated Common Solutions"
    service=""
    resource=""
    authors="jaserano, v-miegge"
    ms.author="jaserano"
    authorAlias="jaserano"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32636888"
    resourceTags=""
    productPesIds="15947"
    cloudEnvironments="public, fairfax, usnat, ussec"
    articleId="bb7af66b-17cd-47cb-8eb0-dfe8078a4ec8"
	ownershipId="Azure_Security_Security_Center"
/>

# Security Alerts - No alerts generated Common Solutions

## Alerts types

* Virtual Machine Behavioral Analysis (VMBA)<br>
* Network Analysis<br>
* SQL Database and SQL Data Warehouse Analysis<br>
* Contextual Information

To enable advanced detections, upgrade to **Azure Security Center Standard**. A free trial is available. To upgrade, select **Pricing Tier** in the [Security Policy](https://gallery.technet.microsoft.com/Azure-Security-Center-f621a046). See [Azure Security Center pricing](https://docs.microsoft.com/azure/security-center/security-center-pricing) to learn more.

Customers can test the VMBA alerts by first checking whether or not the monitoring agent on the Virtual Machine (VM) is healthy and sending security data to the workspace.

To test the VMBA alerts, go to **Security Center** > **Computer & apps** > **VMs and computers**, then select the relevant computer.

When you see the monitoring status of **Monitored by Azure Security Center**, run alert simulation to check the alert pipeline [Alerts Validation in Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-alert-validation).

In addition to this test, customers can use our playbooks to generate wide range of alerts:<br>

* [Playbook 1](https://gallery.technet.microsoft.com/Azure-Security-Center-549aa7a4)<br>
* [Playbook 2](https://gallery.technet.microsoft.com/Azure-Security-Center-f621a046)

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
