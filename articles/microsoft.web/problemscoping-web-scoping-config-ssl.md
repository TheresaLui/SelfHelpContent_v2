<properties
	pageTitle="Scoping questions for Configuring SSL"
	description="Configuring SSL"
	service="microsoft.web"
	authors="shrahman"
   selfHelpType="problemScopingQuestions"
	supportTopicIds="32440123"
	productPesIds="14748"
	cloudEnvironments="public"
   schemaVersion="1"
   articleId="e8fd8bda-5616-44d8-8980-bceb60ad2973"
/>

# Configuring SSL
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
                    "text": "Are you using an App Service Certificate or an external certificate?"
                },
                {
                    "text": "What domain is the SSL cert issued to?"
                },
                {
                    "text": "What error are you seeing and when are you seeing it?"
                },
                {
                    "text": "What is the name of the App Service?"
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