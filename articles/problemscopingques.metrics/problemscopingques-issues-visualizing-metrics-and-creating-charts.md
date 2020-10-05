<properties
	articleId="problemscopingques-issues-visualizing-metrics-and-creating-charts"
	pageTitle="Issues visualizing metrics and creating charts"
	description="Issues visualizing metrics and creating charts"
	authors="neilghuman"
	ms.author="neghuman"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32677615, 32677616, 32677617, 32677618, 32677619, 32677620"
	productPesIds="16250"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	schemaVersion="1"
	ownershipId="AzureMonitoring_AzureMetrics"
/>
# Issues visualizing metrics and creating charts
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Issues visualizing metrics and creating charts",
    "fileAttachmentHint": "Please upload a screenshot of the issue.",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start happening?",
            "required": false
        },
        {
			"id": "user_experience",
			"order": 3,
			"controlType": "dropdown",
			"displayLabel": "Which user experience are you utilizing?",
            "required": true,
			"watermarkText": "Choose an option",
			"dropdownOptions": [
                {
					"value": "Metrics Explorer",
					"text": "Metrics Explorer"
				},
                {
					"value": "Workbook",
					"text": "Workbook"
				},
                                {
					"value": "dont_know_answer",
					"text": "Don't know answer"
				}
			]
		},
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide details of the metrics that you are trying to work with.",
            "watermarkText": "Provide details of the metrics that you are trying to work with.",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Metric names."
                },
                {
                    "text": "Please upload a screenshot of the problem."
                }
            ]
        },
        {
            "id": "additional_information",
            "order": 9,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional information about the issue.",
            "watermarkText": "Provide any additional information about the issue.",
            "required": false,
            "useAsAdditionalDetails": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---