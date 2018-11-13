<properties
	pageTitle="Scoping questions for Configuring hybrid connections with App Service"
	description="Configuring hybrid connections with App Service"
	service="microsoft.web"
	authors="shrahman"
   selfHelpType="problemScopingQuestions"
	supportTopicIds="32581613"
	productPesIds="14748"
	cloudEnvironments="public"
   schemaVersion="1"
   articleId="e1e848fd-cac2-4473-81a4-b523796daf93"
/>

# Configuring hybrid connections with App Service


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
                    "text": "What is the Hybrid Connection URL? (You can find this in the Hybrid Connection Manager details for the HC or in the connection string shown in the portal.)"
                },
                {
                    "text": "What is the status of the HC? (\"Not connected\", \"Connected\", \"Status unknown\", etc.)"
                },
                {
                    "text": "What is the HC endpoint? (The endpoint that is visible in the Azure portal.)"
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