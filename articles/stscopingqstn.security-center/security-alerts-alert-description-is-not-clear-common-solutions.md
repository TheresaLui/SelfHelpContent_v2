<properties
    pageTitle="Security Alerts - Alert Description is Not Clear Common Solutions"
    description="Security Alerts - Alert Description is Not Clear Common Solutions"
    service=""
    resource=""
    authors="jaserano, v-miegge"
    ms.author="jaserano"
    authorAlias="jaserano"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32636851,32636857,32636861"
    resourceTags=""
    productPesIds="15947"
    cloudEnvironments="public, fairfax, usnat, ussec"
    articleId="255da1d8-c2be-4d0c-ba5c-826d48e92675"
	ownershipId="Azure_Security_Security_Center"
/>

# Security Alerts - Alert Description is Not Clear Common Solutions

In the Description field you can find more details about the security alert event. These additional details offer insight into what triggered the security alert, the target resource, the source IP address (when applicable), and recommendations about how to remediate the issue. In some instances, the source IP address is empty because not all Windows security events logs include the IP address.

The remediation suggested by Security Center varies according to the security alert. In some situations, you may have to use other Azure capabilities to implement the recommended remediation. For example, the remediation for this attack is to blacklist the IP address that is generating this attack. To do this, use a [virtual network ACL](https://docs.microsoft.com/azure/virtual-network/virtual-networks-acl) or a [network security group](https://docs.microsoft.com/azure/virtual-network/security-overview#security-rules) rule. For more information on the different types of alerts, read [Security Alerts by Type in Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-alerts-type).

Customers can share feedback for the alert description and relevance. Navigate to the alert itself, select the **Was This Useful** button, select the reason, and enter a comment to explain the feedback. We consistently monitor this feedback channel to improve our alerts.

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
