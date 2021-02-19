<properties
  pagetitle="Azure Security Center Regulatory Compliance self-help guide"
  ms.author="elsagie"
  selfhelptype="Generic"
  supporttopicids="32693246"
  resourcetags=""
  productpesids="15947"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="a15f057d-9001-8910-a98a-dfaf3843dc2f"
  ownershipid="Azure_Security_Security_Center" />
# Azure Security Center Regulatory Compliance self-help guide

Use these resources to resolve common issues with Azure Security Center (ASC) compliance. 


## Supported ASC Regulatory Compliance Standards

ASC Regulatory Compliance supports the following compliance standards by default:

* Azure Security Benchmark
* PCI DSS 3.2.1
* ISO 27001
* SOC TSP

These standards appear in your Security Policy management portal "out of the box."  
Azure Security Benchmark was developed by Microsoft for security and compliance best practices on the Azure portal, based on common compliance frameworks.  
Learn more about [Azure Security Benchmark](https://docs.microsoft.com/azure/security/benchmarks/introduction).


## Regulatory Compliance management

- You can add standards such as Azure CIS 1.1.0 (new), HIPAA/HITRUST, NIST SP 800-53 R4, SWIFT CSP CSCF-v2020, UK Official and UK NHS, Canada Federal PBMM, and others as they become available.  
   For documentation on these standards, see [Customizing the set of standards in your regulatory compliance dashboard](https://docs.microsoft.com/azure/security-center/update-regulatory-compliance-packages)
- Custom Policy initiatives can be assigned to your subscription and appear under the ASC Regulatory Compliance portal.  
Learn how to: [Using custom security policies](https://docs.microsoft.com/azure/security-center/custom-security-policies)


## Common scenarios questions
- This public page is dynamically updated with common scenarios:  
[FAQ - Regulatory compliance dashboard](https://docs.microsoft.com/azure/security-center/security-center-compliance-dashboard#faq---regulatory-compliance-dashboard)


## Troubleshooting

- The Compliance dashboard displays security assessments and recommendations as they align to specific compliance requirements. If a recommendation result is inaccurate, unresolved, or presents an unexpected health status, refer to [Remediate recommendations in Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-remediate-recommendations).

## Known issues and limitations
- Customization within the **Regulatory Compliance** blade is not supported. For example, a customer receives the PCI DSS 3.2 report for the whole subscription, but only wants the PCI-DSS 3.2 report for a selected resource group. Unfortunately, it's not possible to modify the value of certain CCEID to match a company's standard.
- A custom initiative is assigned to the subscription, but isn't visible from the Regulatory Compliance dashboard.   
Check that your initiative doesn't contain a built-in security policy, as it may conflict with ASC default recommendations.


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
