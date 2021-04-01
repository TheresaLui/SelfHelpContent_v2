<properties
  pagetitle="Azure Policy - Policy enforcement not as expected&#xD;"
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

Use the following steps if Azure Policy policy enforcement is not as expected.

## **Recommended Steps**

1.  Allow approximately 30 minutes for policy effect and compliance data to propagate. 
2.  Verify that the correct [policy definition mode](https://docs.microsoft.com/azure/governance/policy/concepts/definition-structure#mode) is being used:
  * Mode all for all resource types 
  * Mode indexed if the policy checks using tags or location
  * Mode that has .Data is not available for any custom policies. Built-in definitions only.
3. Verify that the effect is correct. If you're using `AuditIfNotExisit` or `DeployIfNotExist`, an existence condition is needed. If you want to monitor with no effect or existence condition, then use Audit. Modify doesn’t require either an ARM template or existence condition. Learn more about [effects](https://docs.microsoft.com/azure/governance/policy/concepts/effects).
4. If adding a tag condition in your policy definition, follow similar logic as [these tag built-in policies](https://docs.microsoft.com/azure/governance/policy/samples/pattern-tags) 
5.  Verify that the resource payload matches the policy definition logic. You can do this check by capturing a [HAR trace](https://docs.microsoft.com/azure/azure-portal/capture-browser-trace) or reviewing the ARM template properties. 
6.  If you duplicated a built-in policy definition to customize the definition _or_ you're authoring a custom definition, create the support ticket under **Authoring a policy** for information and help that fits your needs.

## **Recommended Documents**

* [Get compliance data](https://docs.microsoft.com/azure/governance/policy/how-to/get-compliance-data)
* [How are arrays evaluated](https://docs.microsoft.com/azure/governance/policy/how-to/author-policies-for-arrays)
* [Troubleshooting steps](https://docs.microsoft.com/azure/governance/policy/troubleshoot/general#scenario-evaluation-not-as-expected)
