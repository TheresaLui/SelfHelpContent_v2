<properties
	pageTitle="Azure Defender - Vulnerability Assessment (VA) - Container image scanning (ACR)"
	description="Azure Defenderr - Vulnerability Assessment (VA) - Container image scanning (ACR)"
	authors="orbarak-ms"
	ms.author="orbarak"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32749414"
    productPesIds="15947"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    articleId="scoping_asc_va_acr"
	schemaVersion="1"
	ownershipId="Azure_Security_Security_Center"
/>
# Configuring Features and Resources - Just-in-time access (JIT)
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "Vulnerability Assessment (VA) - Container image scanning (ACR)",
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
                            "value": "Image scan is missing",
                            "text": "Image scan is missing"
                        },
                        {
                            "value": "Deleted image findings remain",
                            "text": "Deleted image findings remain"
                        },
                        {
                            "value": "Scan completed but there are no findings",
                            "text": "Scan completed but there are no findingse"
                        },
                        {
                            "value": "Scan Error",
                            "text": "Scan Error"
                        },                        {
                            "value": "dont_know_answer",
                            "text": "Other"
                        }
                    ],
                    "required": true
                },{
                    "id": "issue_location",
                    "order": 3,
                    "controlType": "dropdown",
                    "displayLabel": "Please select Container Registry Type",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                        {
                            "value": "Public",
                            "text": "Public"
                        },
                        {
                            "value": "Private (Firewalled)",
                            "text": "Private (Firewalled)"
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
