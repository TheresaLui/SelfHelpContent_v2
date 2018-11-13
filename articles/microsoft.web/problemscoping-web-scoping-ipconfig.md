<properties
	pageTitle="Scoping questions for IP configuration"
	description="IP configuration"
	service="microsoft.web"
	authors="shrahman"
   selfHelpType="problemScopingQuestions"
	supportTopicIds="32542210"
	productPesIds="14748"
	cloudEnvironments="public"
   schemaVersion="1"
   articleId="1b5ede53-d34b-4f95-933f-92355b9f7e7f"
/>

# IP configuration
---
{
    "resourceRequired": false,
    "formElements": [
        {
            "id": "problem_description",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "hints": [
                {
                    "text": "What is the name of your App Service?"
                },
                {
                    "text": "Does your App Service have a custom domain with an IP-based SSL binding on it?"
                },
                {
                    "text": "Are you looking to set up IP restrictions or are the current settings not working?"
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
    ]
}
---