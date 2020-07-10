<properties
	articleId="problemscopingques-function-app-restarted"
	pageTitle="Function App restarted"
	description="Function App restarted"
	supportTopicIds="32630467"
	authors="khaled-zayed"
	ms.author="khzayed"
	selfHelpType="problemScopingQuestions"
	productPesIds="16072"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="Compute_AppService"
/>
# Function App restarted
---
{
    "resourceRequired": false,
    "title": "Function App restarted",
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
            "id": "4",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "How did you detect that a restart occurred?",
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
