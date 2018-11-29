<properties
	pageTitle="Storage Account creation issues"
	description="Issues creating Storage Account scoping question"
	authors="Passaree"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32602693"
	productPesIds="15629"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Issues creating Storage Account
---
{
    "resourceRequired": false,
    "title": "Storage Account creation issue",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "storage_account_name",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Name of Storage Account that failed to create",
            "required": true
        },
        {
            "id": "storage_account_region",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Region for Storage Account",
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate time when account creation failed",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional details",
            "required": false,
            "useAsAdditionalDetails": true
        }
    ]
}
---