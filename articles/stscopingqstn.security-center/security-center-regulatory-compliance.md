<properties
    pageTitle="Azure Security Center Regulatory Compliance Common Solutions"
    description="Azure Security Center Regulatory Compliance Common Solutions"
    authors="genlin, v-miegge"
    ms.author="jaserano, kawilson"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32693246"
    resourceTags=""
    productPesIds="15947"
    cloudEnvironments="public, fairfax, usnat, ussec"
    articleId="a15f057d-9001-8910-a98a-dfaf3843dc2f"
	ownershipId="Azure_Security_Security_Center"
/>

# Azure Security Center Regulatory Compliance Common Solutions 

## Common Regulatory Compliance issues

**Supported Azure Security Center Regulatory Compliance Standards**

ASC Regulatory Compliance currently only supports the following Compliance Standards:

* Azure CIS
* PCI DSS 3.2
* ISO 27001
* SOC TSP

Additional standards will be reflected in the dashboard as it develops.

**On Security Center CIS regulatory compliance some assessments appear grayed out**

Select a tab for a compliance standard that is relevant to you. You will see the list of all controls for that standard. For the applicable controls, you can view the details of passing and failing assessments associated with that control. Some controls are grayed out. These controls do not have any Security Center assessments associated with them. [See here for more information](https://docs.microsoft.com/azure/security-center/security-center-compliance-dashboard#assess-your-regulatory-compliance).

**Note**: Customizations within the Regulatory Compliance blade is not supported. Example: Customer received the PCI DSS 3.2 report for the whole subscription. The customer would like to download PCI-DSS 3.2 report only for a selected resource group. It is not possible to modify the value of certain CCEID to match your companies standard.

**I made the suggested changed based on the recommendation, yet it is not being reflected in the dashboard**

After you take action to resolve recommendations, please await 12 hours to see the impact on your compliance data. Assessments are run approximately every 12 hours, so you will see the impact on your compliance data only after the assessments run.

## Additional information

To use the Regulatory Compliance, Azure Security Center must be on standard pricing tier on the subscription level. If the Regulatory Compliance UI is not loading correctly, try the following steps:

1. Clear browser cache
1. Use a different browser
1. Try to load it from different network location

The compliance dashboard surfaces security assessments and recommendations as they align to specific compliance requirements. If a recommendation result is not accurate, refer to the recommendation section for further analysis.

## **Recommended Documents**

* [Azure Security Center Compliance Dashboard](https://docs.microsoft.com/azure/security-center/security-center-compliance-dashboard)<br>
* [Azure Security Center Using Custom Security Policies](https://docs.microsoft.com/azure/security-center/custom-security-policies)
<br>
* [Azure Security Center Pricing Tiers](https://docs.microsoft.com/azure/security-center/security-center-pricing)


### Troubleshooting

* [Azure Security Center Troubleshooting Guide](https://docs.microsoft.com/azure/security-center/security-center-troubleshooting-guide)

### FAQ

* [Azure Security Center FAQ](https://docs.microsoft.com/azure/security-center/security-center-faq)
