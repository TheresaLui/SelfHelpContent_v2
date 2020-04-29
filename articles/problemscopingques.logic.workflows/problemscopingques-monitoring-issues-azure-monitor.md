<properties
	articleId="problemscopingques-azure-monitor"
	pageTitle="Azure Monitor"
	description="Azure Monitor"
	supportTopicIds="32588754"
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
    "title": "Azure Monitor",
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
            "id": "2",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Was this Logic App working previously?",
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
            "id": "3",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Please provide one or more Run IDs related to this incident.",
            "watermarkText": "Run IDs...",
            "required": false
        },
        {
            "id": "4",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Please provide the resource IDs of Logic Apps with similar symptoms.",
            "watermarkText": "Resource IDs...",
            "required": false
        },
        {
            "id": "5",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "Please provide the resource IDs of Logic Apps with the same overall structure and connectors that are not experiencing the same symptoms.",
            "watermarkText": "Resource IDs...",
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
