<properties
    pageTitle="Azure Lighthouse - TenantSubscription ID"
    description="Azure Lighthouse - TenantSubscription ID"
    ms.author="prukulka"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32642164, 32642165, 32642166, 32642168, 32642169, 32642170"
    productPesIds="16761"
    articleId="problemscopingques- tenant-subscriptioninfo.md"
    cloudEnvironments="public, fairfax, usnat"
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
            "id": "problem_description",
            "order": 2,
            "controlType": "Textbox",
            "displayLabel": "HAR/fiddler trace or any other error message (if applicable)",
            "watermarkText": "Provide the HAR/fiddler trace or any error message or additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": 
            [
                {
                    "text": "Issue description."
                }
            ]
        }, {
            "id": "ManagedByTenantID_desc",
            "order": 3,
            "controlType": "Textbox",
            "displayLabel": "Managing tenant ID(if applicable)",
            "watermarkText": "Please provide the ID of the tenant that is managing the services(if applicable)",
            "required": false   
        }, {
            "id": "OtherSubID_desc",
            "order": 4,
            "controlType": "Textbox",
            "displayLabel": "Other Subscription ID that is impacted with the same issue(if applicable)",
            "watermarkText": "Please provide other subscription ID that is impacted with this same issue(if applicable)",
            "required": false
        }
	]
}
---