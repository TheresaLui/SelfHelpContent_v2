<properties
	pageTitle="Azure Defender - File Integrity Monitoring (FIM)"
	description="Azure Defenderr - File Integrity Monitoring (FIM)"
	authors="orbarak-ms"
	ms.author="orbarak"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32693232"
    productPesIds="15947"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    articleId="scoping_asc_fim"
	schemaVersion="1"
	ownershipId="Azure_Security_Security_Center"
/>
# Configuring Features and Resources - Just-in-time access (JIT)
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "File Integrity Monitoring (FIM)",
				"subscriptionRequired": false,
                "formElements": [
                {
                    "id": "issue_type",
                    "order": 2,
                    "controlType": "dropdown",
                    "displayLabel": "Please select the issue you are requesting support for",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                        {
                            "value": "Changes are not being tracked",
                            "text": "Changes are not being tracked"
                        },
                        {
                            "value": "Workspace for FIM",
                            "text": "Workspace for FIM"
                        },
                        {
                            "value": "Querying for changes in the workspace",
                            "text": "Querying for changes in the workspace"
                        },                        {
                            "value": "dont_know_answer",
                            "text": "Other FIM Issue"
                        }
                    ],
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
