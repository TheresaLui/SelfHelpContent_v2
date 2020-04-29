<properties
	articleId="problemscopingques-arm-deployment"
	pageTitle="ARM Deployment"
	description="ARM Deployment"
	supportTopicIds="32588752"
	authors="khaled-zayed"
	ms.author="khzayed"
	selfHelpType="problemScopingQuestions"
	productPesIds="15791"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="Compute_LogicApps"
/>
# On-Premises Data Gateway
---
{
    "resourceRequired": false,
    "title": "ARM Deployment",
    "fileAttachmentHint": "Please provide screenshots showing the error or any relevant files",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "Incident time",
            "required": true
        },
        {
            "id": "4",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Please provide the resource IDs of Logic Apps with similar symptoms.",
            "watermarkText": "Resource IDs...",
            "required": false
        },
        {
            "id": "5",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Please provide the resource IDs of Logic Apps with the same overall structure and connectors that are not experiencing the same symptoms.",
            "watermarkText": "Resource IDs...",
            "required": false
        },
        {
            "id": "json",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "If you can’t save or update your definition, please share this JSON code with us.",
            "watermarkText": "JSON code...",
            "required": false
        },
        {
            "id": "deploy",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Were you able to deploy before to this Logic App without errors?",
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
