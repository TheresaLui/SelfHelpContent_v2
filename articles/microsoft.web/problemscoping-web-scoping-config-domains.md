<properties
	pageTitle="Scoping questions for Configuring custom domain names"
	description="Configuring custom domain names"
	service="microsoft.web"
	authors="shrahman"
   selfHelpType="problemScopingQuestions"
	supportTopicIds="32440122"
	productPesIds="14748"
	cloudEnvironments="public"
   schemaVersion="1"
   articleId="9314bc56-da73-49ab-951c-93cba03e0ab2"
/>

# Configuring custom domain names

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
                    "text": "What is the name of the App Service?"
                },
                {
                    "text": "What is the custom domain?"
                },
                {
                    "text": "Is this an App Service Domain or an externally hosted domain?"
                },
                {
                    "text": "What error are you seeing and when are you seeing it?"
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