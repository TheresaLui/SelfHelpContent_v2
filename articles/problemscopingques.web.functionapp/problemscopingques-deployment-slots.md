<properties
	articleId="problemscopingques-deployment-slots"
	pageTitle="Deployment Slots"
	description="Deployment Slots"
	supportTopicIds="32630465"
	authors="khaled-zayed"
	ms.author="khzayed"
	selfHelpType="problemScopingQuestions"
	productPesIds="16072"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="Compute_AppService"
/>
# On-Premises Data Gateway
---
{
    "resourceRequired": false,
    "title": "Connectivity - On-Premises Data Gateway",
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
            "displayLabel": "If you are trying to swap slots, are you using regular Slot Swap or Swap with Preview?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Slot Swap",
                    "text": "Slot Swap"
                },
                {
                    "value": "Swap with Preview",
                    "text": "Swap with Preview"
                }
            ],
            "required": false
        },
        {
            "id": "3",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What exception are you experiencing?",
            "watermarkText": "...",
            "required": false
        },
        {
            "id": "4",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Can you provide the Activity Log entry for this slot action?",
            "watermarkText": "...",
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
