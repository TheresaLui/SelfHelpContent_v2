<properties
	articleId="problemscopingques-arm-templates"
	pageTitle="ARM Templates"
	description="ARM Templates"
	supportTopicIds="32630462"
	authors="khaled-zayed"
	ms.author="khzayed"
	selfHelpType="problemScopingQuestions"
	productPesIds="16072"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="Compute_AppService"
/>
# ARM Templates
---
{
    "resourceRequired": false,
    "title": "ARM Templates",
    "fileAttachmentHint": "Please attach the ARM template you are using as well as any relevant logs/screenshots",
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
            "displayLabel": "Does the exception occur during the deployment of the application code or with the building out and configuration of the infrastructure?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Deployment of the application code",
                    "text": "Deployment of the application code"
                },
                {
                    "value": "Building out and configuration of the infrastructure",
                    "text": "Building out and configuration of the infrastructure"
                }
            ],
            "required": false
        },
        {
            "id": "3",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What deployment exception are you experiencing?",
            "watermarkText": "exception...",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 4,
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
