<properties
	pageTitle="Azure Defender - Recommendation Exemption"
	description="Azure Defenderr - Recommendation Exemption"
	authors="orbarak-ms"
	ms.author="orbarak"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32693235"
    productPesIds="15947"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    articleId="scoping_asc_recommendationexemption"
	schemaVersion="1"
	ownershipId="Azure_Security_Security_Center"
/>
# Configuring Features and Resources - Just-in-time access (JIT)
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "Recommendation Exemption",
				"subscriptionRequired": false,
                "formElements": [
                {
                    "id": "issue_type",
                    "order": 2,
                    "controlType": "dropdown",
                    "displayLabel": "Scope of the exemption",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                        {
                            "value": "Management Group",
                            "text": "Management Group"
                        },
                        {
                            "value": "Subscription",
                            "text": "Subscription"
                        },
						{
                            "value": "Resources",
                            "text": "Resources"
                        },
                        {
                            "value": "dont_know_answer",
                            "text": "Other"
                        }
                    ],
                    "required": true
                },{
                "id": "init_name",
                "order": 3,
                "controlType": "textbox",
                "displayLabel": "Names of the Recommendations in concern",
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
