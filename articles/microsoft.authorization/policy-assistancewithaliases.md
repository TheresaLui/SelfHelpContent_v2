<properties
    pageTitle="Assistance with aliases"
    description="Assistance with aliases"
    service="microsoft.authorization"
    resource="policyDefinitions"
    authors="robga"
    ms.author="robga"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32739632"
    resourceTags=""
    productPesIds="16456"
    cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
    articleId="b3344bfb-13b6-4348-aa55-01b6700530e0"
    ownershipId="Compute_AzurePolicy"
/>

# Azure Policy - Assistance with aliases

## **Recommended Steps**

* **Which resources are covered by Policy?**

We support all resources that go through the Azure Resource Manager (ARM). We also have previews of built-in policies for the following data-plane resources: [AKS](https://docs.microsoft.com/azure/governance/policy/concepts/rego-for-aks), [AKS Engine](https://docs.microsoft.com/azure/governance/policy/concepts/aks-engine), and [Key Vault](https://docs.microsoft.com/azure/governance/policy/samples/keyvault-no-vnet-rules). You can also use [Guest Config on VMs](https://docs.microsoft.com/azure/governance/policy/concepts/guest-configuration) with policy.


* **Alias not found/not working**

If an alias isn't working, be sure to validate that the [alias](https://docs.microsoft.com/azure/governance/policy/tutorials/create-custom-policy-definition#find-the-property-alias) exist and maps to the correct resource type.
The easiest way to find an alias to a resource property is by using our [VS Code extension](https://docs.microsoft.com/azure/governance/policy/how-to/extension-for-vscode). Other ways to find an alias found [here](https://docs.microsoft.com/azure/governance/policy/concepts/definition-structure#aliases).
If an alias does not exist, create a support ticket.
