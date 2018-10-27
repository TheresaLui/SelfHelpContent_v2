<properties
	pageTitle="Scoping questions for VNET integration with App Service"
	description="VNET integration with App Service"
	service="microsoft.web"
	authors="shrahman"
   selfHelpType="problemScopingQuestions"
	supportTopicIds="32542212"
	productPesIds="14748"
	cloudEnvironments="public"
   schemaVersion="1"
   articleId="28446461-8c33-42b3-984e-0d378ea3bbf1"
/>

# VNET integration with App Service
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
                    "text": "What is the name of VNET"
                },
                {
                    "text": "What is the Gateway type configured with existing VNET?"
                },
                {
                    "text": "Is point-to-site enabled on VNET Gateway?"
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