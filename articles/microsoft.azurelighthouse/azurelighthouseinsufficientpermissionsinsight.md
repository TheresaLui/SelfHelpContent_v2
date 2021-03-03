<properties
  pageTitle="Azure Lighthouse Resource Delegation Failure"
  description="Lighthouse delegation failed due to insufficient permissions for Lighthouse resource creation"
  infoBubbleText="Lighthouse delegation failed due to permissions error. See details on the right."
  service="microsoft.managedservices"
  resource="registrationdefinitions"
  ms.author="dabooher"
  displayOrder=""
  articleId="azurelighthouseinsufficientpermissionsinsight"
  diagnosticScenario="azurelighthouseinsufficientpermissionsinsight"
  selfHelpType="diagnostics"
  supportTopicIds="0ae92c46-c05e-9fd8-aefc-6c9b75508907,02aec9c7-431f-adb8-ee6f-ee7af8b7bf26"
  resourceTags=""
  productPesIds="16761"
  cloudEnvironments="public,fairfax,mooncake, usnat, ussec"
  ownershipId="Compute_AzureLighthouse"
/>

# Azure Lighthouse Resource Delegation Failure

## **Recommended Steps**

**Resource delegation must be done by a subscription owner**
<!--issueDescription-->
We've noticed that you're receiving errors related to your permissions while trying to delegate resources using Azure Lighthouse. Azure Lighthouse resource delegation is intentionally limited to subscription owners in order to prevent resources from being improperly delegated to scopes outside of the resource creator's control. If the principal you use to create an Azure Lighthouse delegation doesn't have the required 'Owner' role on the subscription, delegation will fail because you aren't allowed create the resources we need for the delegation to operate. When creating Azure Lighthouse delegations, please make sure that you do so from a principal which has the required 'Owner' role.
<!--/issueDescription-->
