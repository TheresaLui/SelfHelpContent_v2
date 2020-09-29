<properties
    pageTitle="Security Policy - Edit policies assignments Common Solutions"
    description="Security Policy - Edit policies assignments Common Solutions"
    service=""
    resource=""
    authors="jaserano, v-miegge"
    ms.author="jaserano"
    authorAlias="jaserano"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32636853,32636872"
    resourceTags=""
    productPesIds="15947"
    cloudEnvironments="public, fairfax, usnat, ussec"
    articleId="10e15626-7ad8-4ca2-8885-74242b55fd0c"
	ownershipId="Azure_Security_Security_Center"
/>

# Security Policy - Edit policies assignments Common Solutions

You can edit the default security policy for each of your Azure subscriptions and management groups in [Azure Policy](https://docs.microsoft.com/azure/governance/policy/tutorials/create-and-manage). To modify a security policy, you must be an owner, contributor, or security administrator of either the subscription or the management group that contains the subscription.

For instructions to edit a security policy in **Azure Policy**, see [Create and manage policies to enforce compliance](https://docs.microsoft.com/azure/governance/policy/tutorials/create-and-manage).

You can edit security policies through the **Azure Policy** portal through the REST API, or by using **Windows PowerShell**. The following example provides instructions for [editing by using the REST API](https://docs.microsoft.com/azure/security-center/tutorial-security-policy#configure-a-security-policy-using-the-rest-api).

Azure Policy has several permissions, known as operations, in the following Resource Providers:

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
