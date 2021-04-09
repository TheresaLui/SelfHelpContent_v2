<properties
	pageTitle="Azure Defender - Portal and UI/Inventory in security center"
	description="Azure Defenderr - Portal and UI/Inventory in security center"
	authors="orbarak-ms"
	ms.author="orbarak"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32788565"
    productPesIds="15947"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    articleId="scoping_asc_portalui_inventory"
	schemaVersion="1"
	ownershipId="Azure_Security_Security_Center"
/>
# Portal and UI/Inventory in security center
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "Portal and UI/Inventory in security center",
				"subscriptionRequired": false,
                "formElements": [
                {
                    "id": "issue_type",
                    "order": 2,
                    "controlType": "dropdown",
                    "displayLabel": "What is the issue type?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                        {
                            "value": "Resource is missing",
                            "text": "Resource is missing"
                        },
                        {
                            "value": "Resource details mismatch",
                            "text": "Resource details mismatch"
                        },
						                        {
                            "value": "CSV Report",
                            "text": "CSV Report"
                        },
                        {
                            "value": "dont_know_answer",
                            "text": "Other"
                        }
                    ],
                    "required": true
                },{
                "id": "resource_type",
                "order": 3,
                "controlType": "textbox",
                "displayLabel": "What is the resource type?",
                "required": true
                },{
                    "id": "problem_description",
                    "order": 1,
                    "controlType": "multilinetextbox",
                    "displayLabel": "Description",
                    "useAsAdditionalDetails": true,
                    "required": true
                    },{
                    "id": "problem_start_time",
                    "order": 8,
                    "controlType": "datetimepicker",
                    "displayLabel": "When did the problem start?",
                    "required": true
                  }
                  ]
}
---
