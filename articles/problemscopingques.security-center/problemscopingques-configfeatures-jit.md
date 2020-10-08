<properties
	pageTitle="Azure Defender - Configuring Features and Resources - Just-in-time access (JIT)"
	description="Azure Defenderr - Configuring Features and Resources - Just-in-time access (JIT)"
	authors="orbarak-ms"
	ms.author="orbarak"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32693237"
    productPesIds="15947"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    articleId="scoping_asc_configfeatures_jit"
	schemaVersion="1"
	ownershipId="Azure_Security_Security_Center"
/>
# Configuring Features and Resources - Just-in-time access (JIT)
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "Data Collection - Workspaces",
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
                            "value": "Configuring JIT Policy",
                            "text": "Configuring JIT Policy"
                        },
                        {
                            "value": "Requesting Access",
                            "text": "Requesting Access"
                        },
                        {
                            "value": "NSG Issue",
                            "text": "NSG Issue"
                        },
                        {
                            "value": "dont_know_answer",
                            "text": "Other"
                        }
                    ],
                    "required": true
                },{
                    "id": "issue_location",
                    "order": 3,
                    "controlType": "dropdown",
                    "displayLabel": "Where did you try to perform the action selected in the previous question?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                        {
                            "value": "Azure Defender JIT portal",
                            "text": "Azure Defender JIT portal"
                        },
                        {
                            "value": "VM Connect blade",
                            "text": "VM Connect blade"
                        },
                        {
                            "value": "Using API/PowerShell/ARM Template/Other",
                            "text": "Using API/PowerShell/ARM Template/Other"
                        },
                        {
                            "value": "dont_know_answer",
                            "text": "Other"
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
