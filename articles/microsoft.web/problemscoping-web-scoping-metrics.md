<properties
	pageTitle="Metrics are not available or are incorrect"
	description="Configuration and Management/Metrics are not available or are incorrect"
	service="microsoft.web"
	authors="shrahman"
   selfHelpType="problemScopingQuestions"
	supportTopicIds="32581617"
	productPesIds="14748"
	cloudEnvironments="public, MoonCake, Fairfax, usnat, ussec"
   schemaVersion="1"
   articleId="bf000ecb-9268-4834-bb7f-6eced0867ded"
	ownershipId="Compute_AppService"
/>

# Metrics are not available or are incorrect
---
{
    "resourceRequired": false,
    "formElements": [
        {
            "id": "problem_description",
            "order": 1,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "hints": [
                {
                    "text": "Which metric is not being shown or is incorrect?"
                },
                {
                    "text": "Is the metric only missing for a specific \"Time range\" view (i.e past hour, past 24 hours etc.)?"
                }
            ]
        },
        {
            "id": "problem_start_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "Problem start time",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---