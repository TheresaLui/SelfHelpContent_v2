<properties
    pageTitle="My problem is not listed here"
    description="My problem is not listed here"
    service="microsoft.authorization"
    resource="policyDefinitions"
    authors="robga"
    ms.author="robga"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32739636"
    resourceTags=""
    productPesIds="16456"
    cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
    articleId="e47a6f09-5c90-46a5-ad54-c4a8d3e39136"
    ownershipId="Compute_AzurePolicy"
/>

# Azure Policy - My problem is not listed here

## **Recommended Steps**

* **How/When are compliance scans triggered?**

Please allow about 15 minutes for the compliance scan to be triggered and get back compliance results. Compliance scan is triggered once it receives notification of resource change and a new scan every 24 hours. If you do not see any results within 24 hours, please create a support ticket. You can trigger on demand scan using REST API and PS, please refer [here](https://docs.microsoft.com/azure/governance/policy/how-to/get-compliance-data#on-demand-evaluation-scan).

* **How do I find an alias?**

To search for an alias, you can run a command or use the VS Code extension. More information [here](https://docs.microsoft.com/azure/governance/policy/tutorials/create-custom-policy-definition#find-the-property-alias).

* **How do I export my compliance data/ How do I export my policy definitions and assignments?**

We currently do not support exporting compliance data through the portal. Please leverage [UserVoice](https://feedback.azure.com/forums/915958-azure-governance?category_id=345055)to vote on your preference for exporting or other features. You can get compliance data through a [Rest API and/or Command line](https://docs.microsoft.com/azure/governance/policy/how-to/get-compliance-data) call. You can use our VS Code extension to export the definitions and assignments.

* **Can I use REGEX within Policy?**

We currently do not support REGEX handling, but it is currently under review. We continue to value your feedback and would appreciate getting more through our [UserVoice](https://feedback.azure.com/forums/915958-azure-governance?category_id=345055). This is a great way to vote on your preference for Regex handling or other features. An alternative for Regex handling is to leverage the [Value](https://docs.microsoft.com/azure/governance/policy/concepts/definition-structure#value) capability which helps you in checking conditions against parameters, template functions, or literals.

* **Why doesn't Modify work for my policy?**

[Modify](https://docs.microsoft.com/azure/governance/policy/concepts/effects#modify) effect is currently **only supported for tags**. Please submit feedback through our [UserVoice](https://feedback.azure.com/forums/915958-azure-governance?category_id=345055) for any feature request.

* **What is Azure Policy for Kubernetes?**

Please follow these links for information on Azure Policy for **Kubernetes**: [AKS](https://docs.microsoft.com/azure/governance/policy/concepts/rego-for-aks) and [AKS Engine](https://docs.microsoft.com/azure/governance/policy/concepts/aks-engine).

* **How can I get information on what's to come for Azure Policy?**

If you are interested in getting more information on what the Azure Policy team is doing, join the quarterly call on Azure Governance [here](https://forms.office.com/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbRxn7UD7lweFDnmuLj72r6E1UN1dLNTBZUVMyNVpHUjJLRE5PVDVGNlkyOC4u)

## **Recommended Documents**

* [Tutorial for creating a custom policy](https://docs.microsoft.com/azure/governance/policy/tutorials/create-custom-policy-definition)
* [Understanding policy assignment](https://docs.microsoft.com/azure/governance/policy/concepts/assignment-structure)
* [Understanding policy definition](https://docs.microsoft.com/azure/governance/policy/concepts/definition-structure)
* [Evaluate impact of a new policy](https://docs.microsoft.com/azure/governance/policy/concepts/evaluate-impact)
* [Get compliance data](https://docs.microsoft.com/azure/governance/policy/how-to/get-compliance-data)
* [Cause of non-compliance](https://docs.microsoft.com/azure/governance/policy/how-to/determine-non-compliance)
