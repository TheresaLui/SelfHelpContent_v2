<properties
  pagetitle="Azure Security Center Regulatory Compliance self-help guide"
  ms.author="jaserano,kawilson,elsagie"
  selfhelptype="Generic"
  supporttopicids="32693246"
  resourcetags=""
  productpesids="15947"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="a15f057d-9001-8910-a98a-dfaf3843dc2f"
  ownershipid="Azure_Security_Security_Center" />
# Azure Security Center Regulatory Compliance self-help guide

## Common Regulatory Compliance issues

### Supported Azure Security Center Regulatory Compliance Standards

ASC Regulatory Compliance currently only supports the following Compliance Standards:

* Azure CIS
* PCI DSS 3.2
* ISO 27001
* SOC TSP

You can add standards such as NIST SP 800-53 R4, SWIFT CSP CSCF-v2020, UK Official and UK NHS, Canada Federal PBMM, and Azure CIS 1.1.0 (new).  
In addition, you can add Azure Security Benchmark, the Microsoft-authored, Azure-specific guidelines for security and compliance best practices based on common compliance frameworks: [Learn more about Azure Security Benchmark](https://docs.microsoft.com/azure/security/benchmarks/introduction).

Additional standards will be reflected in the dashboard as it develops and documented here: [Customizing the set of standards in your regulatory compliance dashboard](https://docs.microsoft.com/azure/security-center/update-regulatory-compliance-packages)

### On Security Center CIS regulatory compliance some assessments appear grayed out

Select a tab for a compliance standard that is relevant to you. You will see the list of all controls for that standard. For the applicable controls, you can view the details of passing and failing assessments associated with that control. Some controls are grayed out. These controls do not have any Security Center assessments associated with them. [See here for more information](https://docs.microsoft.com/azure/security-center/security-center-compliance-dashboard#assess-your-regulatory-compliance).

**Note**: Customizations within the Regulatory Compliance blade is not supported. Example: Customer received the PCI DSS 3.2 report for the whole subscription. The customer would like to download PCI-DSS 3.2 report only for a selected resource group. It is not possible to modify the value of certain CCEID to match your companies standard.

### I made the suggested changed based on the recommendation, yet it is not being reflected in the dashboard

After you take action to resolve recommendations, please await 12 hours to see the impact on your compliance data. Assessments are run approximately every 12 hours, so you will see the impact on your compliance data only after the assessments run.

### Additional information

To use the Regulatory Compliance, Azure Security Center must be on standard pricing tier on the subscription level. If the Regulatory Compliance UI is not loading correctly, try the following steps:

1. Clear browser cache
1. Use a different browser
1. Try to load it from different network location

The compliance dashboard surfaces security assessments and recommendations as they align to specific compliance requirements. If a recommendation result is not accurate, refer to the recommendation section for further analysis.

## **Recommended Documents**

* [Tutorial: Improve your regulatory compliance](https://docs.microsoft.com/azure/security-center/security-center-compliance-dashboard)
* [Using custom security policies](https://docs.microsoft.com/azure/security-center/custom-security-policies)
* [Overview of compliance packages](https://docs.microsoft.com/azure/security-center/update-regulatory-compliance-packages)
* [Azure Security Center Pricing Tiers](https://docs.microsoft.com/azure/security-center/security-center-pricing)
* [Working with security policies](https://docs.microsoft.com/azure/security-center/tutorial-security-policy)
* [Azure Security Benchmark Doc site](https://docs.microsoft.com/azure/security/benchmarks/introduction)

### Troubleshooting

* [Azure Security Center Troubleshooting Guide](https://docs.microsoft.com/azure/security-center/security-center-troubleshooting-guide)

### FAQ

* [Azure Security Center FAQ](https://docs.microsoft.com/azure/security-center/security-center-faq)