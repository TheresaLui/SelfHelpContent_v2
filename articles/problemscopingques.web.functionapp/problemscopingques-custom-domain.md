<properties
	articleId="problemscopingques-custom-domain"
	pageTitle="Custom Domain"
	description="Custom Domain"
	supportTopicIds="32630463"
	authors="khaled-zayed"
	ms.author="khzayed"
	selfHelpType="problemScopingQuestions"
	productPesIds="16072"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="Compute_AppService"
/>
# Custom Domain
---
{
    "resourceRequired": false,
    "title": "Custom Domain",
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
            "displayLabel": "Is this an App Service Domain or an externally hosted domain?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "App Service Domain",
                    "text": "App Service Domain"
                },
                {
                    "value": "External",
                    "text": "External"
                }
            ],
            "required": false
        },
        {
            "id": "3",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What is the custom domain that you are trying to add?",
            "watermarkText": "custom domain...",
            "required": false
        },
        {
            "id": "4",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "What error are you seeing and when are you seeing it?",
            "watermarkText": "error...",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 5,
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
