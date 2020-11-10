<properties
    pageTitle="Security Policy - Enable or Disable security monitoring Common Solutions"
    description="Security Policy - Enable or Disable security monitoring Common Solutions"
    service=""
    resource=""
    authors="jaserano, v-miegge"
    ms.author="jaserano"
    authorAlias="jaserano"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32636873"
    resourceTags=""
    productPesIds="15947"
    cloudEnvironments="public, fairfax, usnat, ussec"
    articleId="b2714188-b181-493c-8a4d-1e69e3e4daf6"
	ownershipId="Azure_Security_Security_Center"
/>

# Security Policy - Enable or Disable security monitoring Common Solutions

If the default security policy is generating a recommendation that is not relevant for your environment, you can disable the policy definition that sends the recommendation. See the [Working with security policies](https://docs.microsoft.com/azure/security-center/tutorial-security-policy#disable-security-policies) article for the necessary steps. Please note that the disable policy changes can take up to twelve (12) hours to take effect.

Azure Policy has several permissions, known as operations, in the following **Resource Providers**:

* [Microsoft.Authorization](https://docs.microsoft.com/azure/role-based-access-control/resource-provider-operations#microsoftauthorization)<br>
* [Microsoft.PolicyInsights](https://docs.microsoft.com/azure/role-based-access-control/resource-provider-operations#microsoftpolicyinsights)

Many built-in roles grant permissions to **Azure Policy** resources. The **Resource Policy Contributor (Preview)** role includes most policy operations. The owner has full rights, the contributor and reader can use all read policy operations, and the contributor can also trigger remediation.

## **Recommended Documents**

* [Azure Security Center Policies](https://docs.microsoft.com/azure/security-center/tutorial-security-policy)<br>
* [Built-in Security Policies in Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-policy-definitions)<br>
* [Create and manage policies to enforce compliance](https://docs.microsoft.com/azure/governance/policy/tutorials/create-and-manage)<br>
* [Overview of the Azure Policy service](https://docs.microsoft.com/azure/governance/policy/overview)

## Troubleshooting

* [ASC Troubleshooting Guide](https://docs.microsoft.com/azure/security-center/security-center-troubleshooting-guide)

## FAQ

* [ASC FAQ](https://docs.microsoft.com/azure/security-center/security-center-faq)
