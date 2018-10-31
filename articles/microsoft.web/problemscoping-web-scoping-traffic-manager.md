<properties
	pageTitle="Scoping questions for Configuring Traffic Manager with App Service"
	description="Configuring Traffic Manager with App Service"
	service="microsoft.web"
	authors="shrahman"
   selfHelpType="problemScopingQuestions"
	supportTopicIds="32581614"
	productPesIds="14748"
	cloudEnvironments="public"
   schemaVersion="1"
   articleId="e62fbea6-244e-4ac6-823e-1f6bce95f331"
/>

# Configuring Traffic Manager with App Service



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
                    "text": "What is the name of Traffic Manager Profile?"
                },
                {
                    "text": "What is the name of the App Service(s) you are configuring Traffic Manager with?"
                },
                {
                    "text": "Are you configuring the App Service(s) as Azure Endpoints or External Endpoints?"
                },
                {
                    "text": "What is the custom domain you are configuring with the Traffic Manager URL?"
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