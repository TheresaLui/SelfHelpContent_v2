<properties
    pageTitle="Policy FAQ"
    description="Policy FAQ"
    service="microsoft.authorization"
    resource="policyDefinitions"
    authors="robga"
    ms.author="robga"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32730225,32730228,32730229,32730230,32730231,32730232,32730233,32730242,32730243"
    resourceTags=""
    productPesIds="16456"
    cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
    articleId="ed334d6b-9bb0-44f2-ae6d-2df6cdfc7334"
    ownershipId="Compute_AzurePolicy"
/>

# Azure Policy - Policy FAQ

## **Recommended Steps**

* **I just assigned my policy but it is not working, what do I do?**

When deploying resources that are expected to apply the policy, please allow around 30 minutes for the policy assignment to take effect. You can log out and log back in to trigger a cache refresh.

* **How/When are compliance scans triggered?**

Please allow about 15 minutes for the compliance scan to be triggered and get back compliance results. Compliance scan is triggered once it receives notification of resource change and a new scan every 24 hours. If you do not see any results within 24 hours, please create a support ticket. To get information on demand scan, please refer [here](https://docs.microsoft.com/azure/governance/policy/how-to/get-compliance-data#on-demand-evaluation-scan).

* **How do I find an alias?**

To search for an alias, you can run a command or use the VS Code extension. More information [here](https://docs.microsoft.com/azure/governance/policy/tutorials/create-custom-policy-definition#find-the-property-alias).

* **How do I export my compliance data?**

We currently do not support exporting compliance data through the portal. Please leverage [UserVoice](https://feedback.azure.com/forums/915958-azure-governance?category_id=345055) to vote on your preference for exporting or other features. You can export compliance data through [a Rest API and/or Command line call](https://docs.microsoft.com/azure/governance/policy/how-to/get-compliance-data).  

* **How do I get alerts?**

To get alerts on Non-compliant Azure policies using Azure Monitor alerts, follow this [tutorial](https://techcommunity.microsoft.com/t5/ITOps-Talk-Blog/How-to-Create-Azure-Monitor-Alerts-for-Non-Compliant-Azure/ba-p/713466).

* **Can I use REGEX within Policy?**

We currently do not support REGEX handling, but it is currently under review. We continue to value your feedback and would appreciate getting more through our [UserVoice](https://feedback.azure.com/forums/915958-azure-governance?category_id=345055). This is a great way to vote on your preference for Regex handling or other features. An alternative for Regex handling is to leverage the [Value](https://docs.microsoft.com/azure/governance/policy/concepts/definition-structure#value) capability which helps you in checking conditions against parameters, template functions or literals.

* **Why doesn’t Modify work for my policy?**

[Modify](https://docs.microsoft.com/azure/governance/policy/concepts/effects#modify) effect is currently only supported for tags. Please submit feedback through our [UserVoice](https://feedback.azure.com/forums/915958-azure-governance?category_id=345055) for any feature request.

* **What is Azure Policy for Kubernetes?**

Please follow these links for information on Azure Policy for Kubernetes: [AKS](https://docs.microsoft.com/azure/governance/policy/concepts/rego-for-aks) and [AKS Engine](https://docs.microsoft.com/azure/governance/policy/concepts/aks-engine).

* **How can I get information on what’s to come for Azure Policy?**

If you are interested in getting more information on what the Azure Policy team is doing, join the monthly call on Azure Governance [here](https://forms.microsoft.com/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbRxPH3jrBa8ZLgoOwxx0Zj5BUQlNBMTZPQVZJRzFYNjBQUDhMSVUwTDRISi4u).