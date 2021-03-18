<properties
	pageTitle="Azure Defender - Vulnerability Assessment (VA) - Built-In (Powered by Qualys)"
	description="Azure Defenderr - Vulnerability Assessment (VA) - Built-In (Powered by Qualys)"
	authors="orbarak-ms"
	ms.author="orbarak"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32749413"
    productPesIds="15947"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    articleId="scoping_asc_va"
	schemaVersion="1"
	ownershipId="Azure_Security_Security_Center"
/>
# Configuring Features and Resources - Just-in-time access (JIT)
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "Vulnerability Assessment (VA) - Built-In (Powered by Qualys)",
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
                            "value": "Qualys VM extension provisioning failure",
                            "text": "Qualys VM extension provisioning failure"
                        },
                        {
                            "value": "Recommendation to install VA solution is missing",
                            "text": "Recommendation to install VA solution is missing"
                        },
                        {
                            "value": "VA findings missing or not updating",
                            "text": "VA findings missing or not updating"
                        },                        {
                            "value": "dont_know_answer",
                            "text": "Other AAC Issue"
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
