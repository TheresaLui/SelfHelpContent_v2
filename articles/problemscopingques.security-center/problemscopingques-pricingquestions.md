<properties
	pageTitle="Azure Defender - Pricing questions"
	description="Azure Defenderr - Pricing questions"
	authors="orbarak-ms"
	ms.author="orbarak"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32749433"
    productPesIds="15947"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    articleId="scoping_asc_pricing_questions"
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
                    "displayLabel": "What is the issue type you are experiencing?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                        {
                            "value": "Pricing resource quantity mismatch",
                            "text": "Pricing resource quantity mismatch"
                        },
                        {
                            "value": "Resource pricing or charges question",
                            "text": "Resource pricing or charges question"
                        },
						{
                            "value": "Fail to enable/disable pricing bundle",
                            "text": "Fail to enable/disable pricing bundle"
                        },
                        {
                            "value": "dont_know_answer",
                            "text": "Other pricing concern"
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
