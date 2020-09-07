<properties
    pageTitle="What resources are covered by Policy"
    description="What resources are covered by Policy"
    service="microsoft.authorization"
    resource="policyDefinitions"
    authors="robga"
    ms.author="robga"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32730239"
    resourceTags=""
    productPesIds="16456"
    cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
    articleId="02605244-09e4-4555-903e-b1a3fef6ead7"
    ownershipId="Compute_AzurePolicy"
/>

# Azure Policy - What resources are covered by Policy

## **Recommended Steps**

* **What resources are covered by Policy?**

We support all resources that go through the Azure Resource Manager. We also have public preview of built-in policies of [AKS](https://docs.microsoft.com/azure/governance/policy/concepts/rego-for-aks), [AKS Engine](https://docs.microsoft.com/azure/governance/policy/concepts/aks-engine), and [Key Vault](https://docs.microsoft.com/azure/governance/policy/samples/keyvault-no-vnet-rules). You can also use [Guest Config on VMs](https://docs.microsoft.com/azure/governance/policy/concepts/guest-configuration) with policy. 

* **Aliases are not found/not working?**

If an aliases is not working, be sure to validate that the [aliases](https://docs.microsoft.com/azure/governance/policy/tutorials/create-custom-policy-definition#find-the-property-alias) exist and is correct. The easiest way to find an aliases is by using our [VS Code extension](https://docs.microsoft.com/azure/governance/policy/how-to/extension-for-vscode) to hover over a resource property.  
If an alias does not exist, create a support ticket. 

* **Is this a issue with Resource Remediation?**

You can "auto-correct" resources using Azure Policy’s [remediate resources](https://docs.microsoft.com/azure/governance/policy/how-to/remediate-resources).
The [DeployIfNotExists](https://docs.microsoft.com/azure/governance/policy/how-to/remediate-resources) effect cannot auto-remediate for delete. If you wish to have a "cannot delete" behavior, please use [resource locks](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-lock-resources).
You can get a list of policy samples in [our documentation](https://docs.microsoft.com/azure/governance/policy/samples/allowed-locations), [Azure-policy GitHub Repo](https://github.com/Azure/azure-policy) and [Community Policy repo](https://github.com/Azure/Community-Policy). 

## **Recommended Documents**

* [Control Plane Aliases](https://docs.microsoft.com/azure/governance/policy/concepts/definition-structure#aliases)
* [Data Plane Aliases - Policy for AKS](https://docs.microsoft.com/azure/governance/policy/concepts/rego-for-aks)
* [Data Plane Aliases - Policy for AKS Engine](https://docs.microsoft.com/azure/governance/policy/concepts/aks-engine)
