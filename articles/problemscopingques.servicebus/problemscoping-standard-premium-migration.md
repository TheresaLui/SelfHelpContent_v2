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
	"formElements": [
		{
            "id": "servicebus_feature",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Service Bus feature",
            "watermarkText": "Choose an option",
            "required": false,
            "dropdownOptions": [{
                "value": "Queues",
                "text": "Queues"
            }, {
                "value": "Topics",
                "text": "Topics"
            }]
        },
        {
            "id": "servicebus_queues",
            "order": 2,
            "controlType": "multiselectdropdown",
            "displayLabel": "Queue names",
            "watermarkText": "Choose an option",
            "required": false,
            "visibility": "servicebus_feature != null && servicebus_feature == Queues",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionid}/resourcegroups/{resourcegroup}/providers/Microsoft.ServiceBus/namespaces/{resourceName}/queues?&api-version=2015-08-01",
                "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "name",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Not applicable/No queues available"
                }
            }
        },
        {
            "id": "servicebus_topics",
            "order": 3,
            "controlType": "multiselectdropdown",
            "displayLabel": "Topic names",
            "watermarkText": "Choose an option",
            "required": false,
            "visibility": "servicebus_feature != null && servicebus_feature == Topics",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionid}/resourcegroups/{resourcegroup}/providers/Microsoft.ServiceBus/namespaces/{resourceName}/topics?&api-version=2015-08-01",
                "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "name",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Not applicable/No topics available"
                }
            }
        },
		{
			"id": "problem_start_time",
			"order": 4,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true
		},
		{
			"id": "problem_migrationmethod",
			"order": 5,
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
			"order": 6,
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
			"order": 7,
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
			"order": 8,
			"controlType": "textbox",
			"displayLabel": "Enter the Post migration namespace",
			"required": true
		},
		{
			"id": "problem_syncstatus",
			"order": 9,
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
			"order": 10,
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
			"order": 11,
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
			"order": 12,
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