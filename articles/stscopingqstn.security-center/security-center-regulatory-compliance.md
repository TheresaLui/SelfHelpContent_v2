<properties
  pagetitle="Azure Security Center Regulatory Compliance self-help guide&#xD;"
  ms.author="elsagie"
  selfhelptype="Generic"
  supporttopicids="32693246"
  resourcetags=""
  productpesids="15947"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="a15f057d-9001-8910-a98a-dfaf3843dc2f"
  ownershipid="Azure_Security_Security_Center" />
# Self-help guide for Azure Security Center Regulatory Compliance

Use these resources to resolve common issues with Azure Security Center (ASC) compliance. 


## Supported ASC Regulatory Compliance Standards

ASC Regulatory Compliance supports the following compliance standards by default:

* Azure CIS 1.1.0
* PCI DSS 3.2.1
* ISO 27001
* SOC2 TSP

You can add standards such as NIST SP 800-53 R4, SWIFT CSP CSCF-v2020, UK Official and UK NHS, Canada Federal PBMM, and Azure CIS 1.1.0 (new).  

In addition, you can add Azure Security Benchmark, which was developed by Microsoft for security and compliance best practices on Azure, based on common compliance frameworks. [Learn more about Azure Security Benchmark](https://docs.microsoft.com/azure/security/benchmarks/introduction).

Additional standards will be reflected in the dashboard as they are developed. For documentation on these standards, see [Customizing the set of standards in your regulatory compliance dashboard](https://docs.microsoft.com/azure/security-center/update-regulatory-compliance-packages)


## Common questions and issues

## On Security Center CIS Regulatory Compliance, some assessments appear grayed out 

Select the tab for a compliance standard to see the list of controls for that standard. For the applicable controls, you can view the details of passing and failing assessments associated with that control. Controls that are grayed out have no Security Center assessments associated with them. Learn more about [assessments](https://docs.microsoft.com/azure/security-center/security-center-compliance-dashboard#assess-your-regulatory-compliance).

**Note**: Customizations within the **Regulatory Compliance** blade are not supported. Example: Customer received the PCI DSS 3.2 report for the whole subscription. The customer would like to download PCI-DSS 3.2 report only for a selected resource group. It is not possible to modify the value of certain CCEID to match a company's standard.

### Can I remove any of the built-in standards that appear by default in the dashboard? I only want to track the additional standards that I onboarded.

Yes. From the **Management | Security Policy** you can disable any of the built-in standards.  

### I made the suggested changes based on the recommendation, yet it is not being reflected in the dashboard

After you take action to resolve recommendations, wait 12 hours to see the impact on your compliance data. Assessments are run approximately every 12 hours, and changes appear only after the assessments run.

### Regulatory Compliance UI is not loading correctly 

To use the Regulatory Compliance, Azure Security Center must be on standard pricing tier on the subscription level. If the Regulatory Compliance UI is not loading correctly, try the following steps:

1. Clear browser cache
1. Use a different browser
1. Try to load it from different network location

The Compliance dashboard displays security assessments and recommendations as they align to specific compliance requirements. If a recommendation result is not accurate, refer to the recommendation section for further analysis.


### Additional troubleshooting

* [Azure Security Center Troubleshooting Guide](https://docs.microsoft.com/azure/security-center/security-center-troubleshooting-guide)


### FAQ

* [Azure Security Center FAQ](https://docs.microsoft.com/azure/security-center/security-center-faq)


## **Recommended Documents**

* [Tutorial: Improve your regulatory compliance](https://docs.microsoft.com/azure/security-center/security-center-compliance-dashboard)
* Blog: [Regulatory compliance dashboard in Azure Security Center](https://azure.microsoft.com/blog/regulatory-compliance-dashboard-in-azure-security-center-now-available/)
* Video: [Compliance Dashboard | Azure Security Center in the Field](https://www.youtube.com/watch?v=dlV1yqPyzQ0)
* Video: [Cloud Security Posture Management (CSPM) with Azure Security Center | Azure Friday](https://www.youtube.com/watch?v=eIoWrBFFusY)
* [Using custom security policies](https://docs.microsoft.com/azure/security-center/custom-security-policies)
* [Overview of compliance packages](https://docs.microsoft.com/azure/security-center/update-regulatory-compliance-packages)
* [Azure Security Center Pricing Tiers](https://docs.microsoft.com/azure/security-center/security-center-pricing)
* [Working with security policies](https://docs.microsoft.com/azure/security-center/tutorial-security-policy)
* [Azure Security benchmarks](https://docs.microsoft.com/azure/security/benchmarks/introduction)
