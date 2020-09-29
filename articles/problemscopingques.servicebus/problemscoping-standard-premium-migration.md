<properties
pageTitle="Standard to Premium SKu Migration"
description="Issues with Standard to Premium SKu Migration"
service="microsoft.servicebus"
resource="skuMigration"
authors="mksuni"
ms.author="mksuni"
displayOrder=""
selfHelpType="problemScopingQuestions"
supportTopicIds="32633407"
resourceTags=""
productPesIds="13186"
cloudEnvironments="public, Fairfax, usnat, ussec"
articleId="sb-sku-migration-issues"
schemaVersion="1"
	ownershipId="AzureMessaging_Common"
/>
# Issues with Standard to Premium SKu Migration
---
{
	"subscriptionRequired": true,
	"resourceRequired": true,
	"title": "Issues with Standard to Premium SKu Migration",
	"fileAttachmentHint": "Please upload any additional information if applicable",
	"formElements": [{
			"id": "problem_start_time",
			"order": 1,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true
		},
		{
			"id": "problem_migrationmethod",
			"order": 2,
			"controlType": "dropdown",
			"displayLabel": "How are you trying to migrate your resource from standard to premium?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "azure_portal",
					"text": "Azure Portal"
				},
				{
					"value": "azure_cli",
					"text": "Azure CLI"
				},
				{
					"value": "powershell",
					"text": "Azure Powershell"
				},
				{
					"value": "dont_know_answer",
					"text": "I Don't Know"
				}
			]
		},
		{
			"id": "problem_namespace",
			"order": 3,
			"controlType": "dropdown",
			"displayLabel": "Are you using a new premium or existing premium namespace?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "new_premium",
					"text": "New Premium Namespace"
				},
				{
					"value": "existing",
					"text": "Existing Premium Namespace"
				},
				{
					"value": "dont_know_answer",
					"text": "I Don't Know"
				}
			]
		},
		{
			"id": "problem_status",
			"order": 4,
			"controlType": "dropdown",
			"displayLabel": "Has the migration completed",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "yes",
					"text": "Yes"
				},
				{
					"value": "no",
					"text": "No"
				},
				{
					"value": "dont_know_answer",
					"text": "I Don't Know"
				}
			]
		},
		{
			"id": "problem_postmigrationnamespace",
			"order": 5,
			"controlType": "textbox",
			"displayLabel": "Enter the Post migration namespace",
			"required": true
		},
		{
			"id": "problem_syncstatus",
			"order": 6,
			"controlType": "dropdown",
			"displayLabel": "Have you copied over all the entities from standard to premium namespace",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "yes",
					"text": "Yes"
				},
				{
					"value": "no",
					"text": "No"
				},
				{
					"value": "dont_know_answer",
					"text": "I Don't Know"
				}
			]
		},
		{
			"id": "problem_drainstatus",
			"order": 7,
			"controlType": "dropdown",
			"displayLabel": "Were you able to successfully drain all entities in the standard namespace by using the post-migration namespace.",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "yes",
					"text": "Yes"
				},
				{
					"value": "no",
					"text": "No"
				},
				{
					"value": "dont_know_answer",
					"text": "I Don't Know"
				}
			]
		},
		{
			"id": "problem_deletestandard",
			"order": 8,
			"controlType": "dropdown",
			"displayLabel": "Have you deleted the standard namespace after migration?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "yes",
					"text": "Yes"
				},
				{
					"value": "no",
					"text": "No"
				},
				{
					"value": "dont_know_answer",
					"text": "I Don't Know"
				}
			]
		},
		{
			"id": "problem_description",
			"order": 9,
			"controlType": "multilinetextbox",
			"displayLabel": "Details",
			"watermarkText": "Provide additional information about your issue",
			"required": true,
			"useAsAdditionalDetails": true,
			"hints": [{
				"text": "Issue description."
			}]
		}
	],
	"$schema": "SelfHelpContent"
}
---