<properties
	pageTitle="Database Connectivity"
	description="Database Connectivity"
	authors="Hang-Zhang"
	ms.author="haz"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32747644"
	productPesIds="17344"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="scoping-mysql-flexsvr-connectivity-ha"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>
# Database Connectivity - Zone redundant HA
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
            "id": "operations",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "What operation you did against the mysql server?",
            "required": false
        },
        {
            "id": "operations",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "How long time the mysql server was unavailable?",
            "required": false
        },
        {
            "id": "ongoing",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Is the issue still ongoing?",
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
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide any driver exceptions/error messages you received and any other information you want to share with us.",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
