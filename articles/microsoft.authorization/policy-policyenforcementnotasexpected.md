<properties
  pagetitle="Azure Policy - Policy enforcement not as expected"
  service="microsoft.authorization"
  resource="policydefinitions"
  ms.author="robga,kenieva"
  selfhelptype="Generic"
  supporttopicids="32739638"
  resourcetags=""
  productpesids="16456"
  cloudenvironments="public,blackforest,fairfax,mooncake,usnat,ussec"
  articleid="1c0cd353-cf08-4d4c-b6cb-a9e73a904872"
  ownershipid="Compute_AzurePolicy" />
# Azure Policy - Policy enforcement not as expected

## **Recommended Steps**

1.	Please allow approximately 30 minutes for policy effect and compliance data
2.	Ensure assignment parameters are correct and assignment scope is as desired. Ensure that [enforcement mode](https://docs.microsoft.com/azure/governance/policy/concepts/assignment-structure#enforcement-mode) is on.
3.	Check the [policy definition mode]( https://docs.microsoft.com/azure/governance/policy/concepts/definition-structure#mode):
  
  * Mode all for all resource types 
  * Mode indexed if the policy checks for tags or location

4.	Check the resource being tested is in the applied scope
5.	Check that the desired scope is not [excluded or exempt]( https://docs.microsoft.com/azure/governance/policy/concepts/scope#assignment-scopes)
6.	Verify the resource payload matches the policy logic. This can be done by capturing a [HAR trace](https://docs.microsoft.com/azure/azure-portal/capture-browser-trace) or reviewing the ARM template properties. 
7.	Check [Troubleshooting information](https://docs.microsoft.com/azure/governance/policy/troubleshoot/general#scenario-evaluation-not-as-expected) for common issues and solutions
8.	If you have duplicated a built-in policy then customize the definition OR are authoring a custom definition, please create the support ticket under 'Authoring a policy' for better suited information and help

## **Recommended Documents**

* [Get compliance data](https://docs.microsoft.com/azure/governance/policy/how-to/get-compliance-data)
* [How are arrays evaluated](https://docs.microsoft.com/azure/governance/policy/how-to/author-policies-for-arrays)
* [Determine causes of non-compliance](https://docs.microsoft.com/azure/governance/policy/how-to/determine-non-compliance)
* [Understanding policy definition](https://docs.microsoft.com/azure/governance/policy/concepts/definition-structure)
* [Understanding policy effects](https://docs.microsoft.com/azure/governance/policy/concepts/effects)
* [Evaluate impact of a new policy](https://docs.microsoft.com/azure/governance/policy/concepts/evaluate-impact)
