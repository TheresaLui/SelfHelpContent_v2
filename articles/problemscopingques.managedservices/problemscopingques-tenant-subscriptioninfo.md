<properties
    pageTitle="Azure Lighthouse - TenantSubscription ID"
    description="Azure Lighthouse - TenantSubscription ID"
    ms.author="prukulka"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32642164, 32642165, 32642166, 32642168, 32642169, 32642170"
    productPesIds="16761"
    articleId="problemscopingques- tenant-subscriptioninfo.md"
    cloudEnvironments="public, fairfax, usnat, ussec"
    ownershipId="Compute_AzureLighthouse"
    schemaVersion="1"
/>
# Tenant-SubscriptionInfo
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": true,
  "resourceRequired": false,
	"title": "Tenant-SubscriptionInfo",
	"fileAttachmentHint": "",
	"formElements": [{
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        }, {
            "id": "Error_Message",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Error Message",
            "watermarkText": "Provide any error messages encountered(if any)",
            "required": false,
            "useAsAdditionalDetails": false
        }, {
            "id": "problem_description",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Issue Description",
            "watermarkText": "Provide any additional details to the issue you're experiencing",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints":
            [
                {
                    "text": "Additional details"
                }
            ]
        }, {
            "id": "ManagedByTenantID_desc",
            "order": 3,
            "controlType": "Textbox",
            "displayLabel": "Managing TenantID",
            "watermarkText": "Please provide the ID of the tenant that is managing the services(if applicable)",
            "required": true
        }, {
            "id": "OtherDelSubID_desc",
            "order": 4,
            "controlType": "Textbox",
            "displayLabel": "ID of the Delegated subscription impacted",
            "watermarkText": "Please provide the delegated subscription ID that is impacted with this same issue(if applicable)",
            "required": true
         }, {
            "id": "PrinicipalID_desc",
            "order": 5,
            "controlType": "Textbox",
            "displayLabel": "Delegated PrincipalID",
            "watermarkText": "Please provide the principalId that is getting the delegated permissions",
            "required": false
        }
	]
}
---