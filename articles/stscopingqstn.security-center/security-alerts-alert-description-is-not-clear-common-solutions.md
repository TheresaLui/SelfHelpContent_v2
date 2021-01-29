<properties
  pagetitle="Security Alerts - Alert investigation self-help guide"
  service=""
  resource=""
  ms.author="elsagie"
  selfhelptype="Generic"
  supporttopicids="32693236"
  resourcetags=""
  productpesids="15947"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="255da1d8-c2be-4d0c-ba5c-826d48e92675"
  ownershipid="Azure_Security_Security_Center" />
# Security Alerts - Alert investigation self-help guide

## **Recommended Steps**

In the Description field for Security Alerts, you can find details about the security alert event. These additional details offer insights into what triggered the security alert, the target resource, the source IP address (when applicable), and recommendations about how to remediate the issue.  

In some instances, the source IP address is empty because not all Windows security events logs include the IP address.

The remediation suggested by Azure Security Center varies according to the security alert. In some situations, you may have to use other Azure capabilities to implement the recommended remediation. For example, the remediation for an attack may be to blacklist the IP address that is generating this attack.  

To do this, use a [virtual network ACL](https://docs.microsoft.com/azure/virtual-network/virtual-networks-acl) or a [network security group](https://docs.microsoft.com/azure/virtual-network/security-overview#security-rules) rule.  

For more information on the different types of alerts, see [Security Alerts by Type in Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-alerts-type).  

You can share feedback for the alert description and relevance. Navigate to the alert itself, select the **Was This Useful** button, select the reason, and enter a comment to explain the feedback. We continuously monitor this feedback channel to improve our alerts.

In addition, [MITRE ATT&CK® tactics](https://docs.microsoft.com/azure/security-center/alerts-reference?WT.mc_id=Portal-Microsoft_Azure_Security#intentions) are indicated for each alert can help you investigate and report the event more easily.

## **Recommended Documents**

* [Tutorial: Respond to security incidents](https://docs.microsoft.com/azure/security-center/tutorial-security-incident)
* [Managing and responding to security alerts in Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-managing-and-responding-alerts)
* [Alerts Validation in Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-alert-validation)
* [Email Notifications in Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-provide-security-contact-details)
* [Handling Security Incidents in Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-incident)
* [Security alerts - a reference guide](https://docs.microsoft.com/azure/security-center/alerts-reference)

## Troubleshooting
* [ASC Troubleshooting Guide](https://docs.microsoft.com/azure/security-center/security-center-troubleshooting-guide)

## FAQ
* [ASC FAQ](https://docs.microsoft.com/azure/security-center/security-center-faq)
