<properties
	articleId="problemscopingques-moving-a-function-app"
	pageTitle="Moving a Function App"
	description="Moving a Function App"
	supportTopicIds="32598329"
	authors="khaled-zayed"
	ms.author="khzayed"
	selfHelpType="problemScopingQuestions"
	productPesIds="16072"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="Compute_AppService"
/>
# Moving a Function App
---
{
    "resourceRequired": false,
    "title": "Moving a Function App",
    "fileAttachmentHint": "Please attach any relevant logs/screenshots",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "Incident time",
            "required": true
        },
        {
            "id": "2",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Are you moving Function App resources within the same subscription or are you moving resources across different subscriptions?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Same subscription",
                    "text": "Same subscription"
                },
                {
                    "value": "Different subscriptions",
                    "text": "Different subscriptions"
                }
            ],
            "required": false
        },
        {
            "id": "3",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What is the source and destination resource group?",
            "watermarkText": "...",
            "required": false
        },
        {
            "id": "4",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Please list all the resources you are trying to move, recognizing that some resources cannot be moved.",
            "watermarkText": "...",
            "required": false
        },
        {
            "id": "5",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Do any of the apps have SSL certificates configured? If yes, are they custom SSL certificates or Azure App Service Certificates?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Custom SSL certificates",
                    "text": "Custom SSL certificates"
                },
                {
                    "value": "Azure App Service Certificates",
                    "text": "Azure App Service Certificates"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Provide additional information about your issue including any error messages you are seeing.",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
