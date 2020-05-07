<properties
	articleId="problemscopingques-timer-trigger-function-failed-to-trigger"
	pageTitle="Timer trigger function failed to trigger"
	description="Timer trigger function failed to trigger"
	supportTopicIds="32630471"
	authors="khaled-zayed"
	ms.author="khzayed"
	selfHelpType="problemScopingQuestions"
	productPesIds="16072"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="Compute_AppService"
/>
# Timer trigger function failed to trigger
---
{
    "resourceRequired": false,
    "title": "Timer trigger function failed to trigger",
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
            "controlType": "textbox",
            "displayLabel": "Please provide the Function name that is not working as expected",
            "watermarkText": "function name...",
            "required": false
        },
        {
            "id": "3",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide the function.json file",
            "watermarkText": "function.json...",
            "required": false
        },
        {
            "id": "5",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Is the Function processing partially or does it time out",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "time out",
                    "text": "time out"
                },
                {
                    "value": "partially",
                    "text": "partially"
                }
            ],
            "required": false
        },
        {
            "id": "7",
            "order": 7,
            "controlType": "dropdown",
            "displayLabel": "Have you made any recent changes to the Azure Storage firewalls and virtual networks?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 8,
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
