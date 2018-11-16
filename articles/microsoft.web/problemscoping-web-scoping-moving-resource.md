<properties
	pageTitle="Scoping questions for Moving resources"
	description="Moving resources"
	service="microsoft.web"
	authors="shrahman"
   selfHelpType="problemScopingQuestions"
	supportTopicIds="32581619"
	productPesIds="14748"
	cloudEnvironments="public, MoonCake"
   schemaVersion="1"
   articleId="73799750-2889-45e0-b6ea-ddb118e38d07"
/>

# Moving resources
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
                    "text": "Are you moving App Service resources within the same subscription or are you trying to move resources across different subscriptions?"
                },
                {
                    "text": "What is the destination resource group?"
                },
                {
                    "text": "What resource(s) are you trying to move?"
                },
                {
                    "text": "Do any of the apps have SSL certificates configured? If yes, are they custom SSL certificates or Azure App Service Certificates?"
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