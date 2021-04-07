<properties
  pagetitle="Azure Policy - Compliance state and details not as expected&#xD;"
  service="microsoft.authorization"
  resource="policydefinitions"
  ms.author="robga,kenieva"
  selfhelptype="Generic"
  supporttopicids="32739633"
  resourcetags=""
  productpesids="16456"
  cloudenvironments="public,blackforest,fairfax,mooncake,usnat,ussec"
  articleid="34a89633-83f9-4b52-a866-d9415078d9cd"
  ownershipid="Compute_AzurePolicy" />
# Azure Policy - Compliance state and details not as expected

If Azure Policy compliance state and details are not as expected, use the following steps.

## **Recommended Steps**

1. Allow approximately 30 minutes for compliance data to populate when first assigning a policy definition (Not Started state) and when updating policy definitions. You can trigger an [on-demand scan]( https://docs.microsoft.com/azure/governance/policy/how-to/get-compliance-data#on-demand-evaluation-scan) using REST API, Azure CLI, Azure PowerShell, or a GitHub Action.
2. Verify that the effect is correct. If you're using `AuditIfNotExisit` or `DeployIfNotExist`, an existence condition is needed. If you want to monitor with no effect or existence condition, then use Audit. Modify doesn’t require either an ARM template or existence condition. Learn more about [effects](https://docs.microsoft.com/azure/governance/policy/concepts/effects).
3.  Ensure assignment parameters are correct and assignment scope is as you want it. Check that the scope you want is not [excluded or exempt](https://docs.microsoft.com/azure/governance/policy/concepts/scope#assignment-scopes). 
4. Keep in mind that for `deployIfNotExist` and `Modify` policy definitions, existing resources aren’t automatically remediated. You need to create a remediation task. 
5.  If compliance says 0/0 resource and the compliance is expected to show resources, then the policy definition isn’t authored correctly or isn’t targeting the expected resource. Revise the custom definition and verify the assignment scope.
6.  Leverage compliance reason details to ensure that the current and target value of the resource are as expected. 
a.  If the target value is incorrect, revise the custom definition. 
b.  If current value is incorrect, validate the resource payload through resources.azure.com. This check can be done by capturing a [HAR trace](https://docs.microsoft.com/azure/azure-portal/capture-browser-trace).
7.  Check [Troubleshooting information](https://docs.microsoft.com/azure/governance/policy/troubleshoot/general#scenario-enforcement-not-as-expected) for common issues and solutions. 
8.  If you duplicated a built-in policy to customize the definition _or_ you're authoring a custom definition, create the support ticket under **Authoring a policy** for information and help that will be useful to you.

## **Recommended Documents**

* [Understanding policy definition](https://docs.microsoft.com/azure/governance/policy/concepts/definition-structure)
