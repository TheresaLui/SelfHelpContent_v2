<properties
	pageTitle="Azure Defender - Issues with enabling Security Center or Azure Defender"
	description="Azure Defenderr - Issues with enabling Security Center or Azure Defender"
	authors="orbarak-ms"
	ms.author="orbarak"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32788563"
    productPesIds="15947"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    articleId="scoping_asc_enabling"
	schemaVersion="1"
	ownershipId="Azure_Security_Security_Center"
/>
# Configuring Features and Resources - Just-in-time access (JIT)
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "Issues with enabling Security Center or Azure Defender",
				"subscriptionRequired": false,
                "formElements": [
                {
                    "id": "issue_type",
                    "order": 2,
                    "controlType": "dropdown",
                    "displayLabel": "Select which resource you are trying to enable",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                        {
                            "value": "Subscription",
                            "text": "Subscription"
                        },
                        {
                            "value": "Log Analytics Workspace",
                            "text": "Log Analytics Workspace"
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
                    "displayLabel": "Describe how you are trying to enable Azure Defender",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                        {
                            "value": "Azure Security Center portal - Pricing & settings",
                            "text": "Azure Security Center portal - Pricing & settings"
                        },
                        {
                            "value": "ARM template",
                            "text": "ARM template"
                        },  
						{
                            "value": "Azure Policy",
                            "text": "Azure Policy"
                        },
                        {
                            "value": "Powershell/API",
                            "text": "Powershell/API"
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
