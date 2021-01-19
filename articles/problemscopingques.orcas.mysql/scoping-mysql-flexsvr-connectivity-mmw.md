<properties
	pageTitle="Database Connectivity"
	description="Database Connectivity"
	authors="Hang-Zhang"
	ms.author="haz"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32747623"
	productPesIds="17344"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="scoping-mysql-flexsvr-connectivity-mmw"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>
# Database Connectivity - managed maintenance window
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Database Connectivity",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "selected_window",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "What is the options and window you selected?",
            "required": false
        },
        {
            "id": "notifications",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "When did you receive notifications?",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know the answer"
                }
            ],
            "required": true
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide any driver exceptions/error messages you received and any other information you want to share with us.",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
