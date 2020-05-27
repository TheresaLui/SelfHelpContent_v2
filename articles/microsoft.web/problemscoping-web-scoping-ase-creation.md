<properties
	pageTitle="Scoping questions for ASE creation"
	description="ASE creation"
	service="microsoft.web"
	authors="shrahman"
   selfHelpType="problemScopingQuestions"
	supportTopicIds="32581608"
	productPesIds="14748"
	cloudEnvironments="public, Fairfax, usnat, ussec"
   schemaVersion="1"
   articleId="22873c27-8f6c-4cee-82df-e50eaacdc600"
	ownershipId="Compute_AppService"
/>

# ASE creation
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
                    "text": "What is the name of the ASE?"
                },
                {
                    "text": "When did the ASE creation start (date and time with time zone)?"
                },
                {
                    "text": "Please provide error you received."
                },
                {
                    "text": "Please provide timestamp (including time zone) of error"
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