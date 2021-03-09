<properties
  pagetitle="Azure Policy - Compliance state and details not as expected"
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

## **Recommended Steps**

1.	Allow approximately 30 minutes for compliance data to populate when first assigning a policy definition (Not Started state) and when updating policy definitions. You can now trigger an [on demand scan]( here) using REST API and PowerShell.
2.	Ensure assignment parameters are correct and assignment scope is as desired. 
3.	Check the [policy definition mode]( https://docs.microsoft.com/azure/governance/policy/concepts/definition-structure#mode). 
a.	Mode all for all resource types 
b.	Mode indexed if the policy checks for tags or location. 
4.	Check that the desired scope is not [excluded or exempt]( https://docs.microsoft.com/azure/governance/policy/concepts/scope#assignment-scopes). 
5.	If compliance says 0/0 resource, yet the compliance is expected to show resources, then the policy definition is not authored correctly and not targeting the resource property that is required. Please revise the custom definition. See step 8.
6.	Leverage compliance reason details to ensure that the current and target value of the resource are as expect. 
a.	If the target value is wrong, please revise the custom definition. See step 8.
b.	If current value is wrong, validate the resource payload through resources.azure.com
7.	Check [Troubleshooting information]( https://docs.microsoft.com/azure/governance/policy/troubleshoot/general#scenario-enforcement-not-as-expected) for common issues and solutions. 
8.	If you have duplicated a built-in policy then customize the definition OR are authoring a custom definition, please create the support ticket under 'Authoring a policy' for better suited information and help.

Keep in mind that for deployIfNotExist and Modify policies, existing resources will not be automatically remediated. You need to create a remediation task. 


## **Recommended Documents**

* [Get compliance data](https://docs.microsoft.com/azure/governance/policy/how-to/get-compliance-data)
* [How are arrays evaluated](https://docs.microsoft.com/azure/governance/policy/how-to/author-policies-for-arrays)
* [Determine causes of non-compliance](https://docs.microsoft.com/azure/governance/policy/how-to/determine-non-compliance)
* [Understanding policy definition](https://docs.microsoft.com/azure/governance/policy/concepts/definition-structure)
* [Understanding policy effects](https://docs.microsoft.com/azure/governance/policy/concepts/effects)
* [Evaluate impact of a new policy](https://docs.microsoft.com/azure/governance/policy/concepts/evaluate-impact)
