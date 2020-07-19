<properties
	articleId="problemscopingques-classicalert-notification"
	pageTitle="Issues with classic alert notifications"
	description="Issues with classic alert notifications"
	authors="snehithm"
	ms.author="snmuvva"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32629657, 32629663, 32629669"
	productPesIds="15454"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureMonitoring_ActionGroup"
/>
# Issues with classic alert notifications
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Issues with notifications",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "notification_type",
            "order": 1,
            "controlType": "multiselectdropdown",
            "displayLabel": "Which type of notifications do you have this problem for?",
            "watermarkText": "Choose one or more notification types",
            "dropdownOptions": [
                {
                    "value": "Email",
                    "text": "Email"
                },
                {
                    "value": "Webhook",
                    "text": "Webhook"
                },
                {
                    "value": "Logic App",
                    "text": "Logic App"
                },
                {
                    "value": "Runbook",
                    "text": "Runbook"
                }
            ],
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Expected behavior, actual behavior"
                },
                {
                    "text": "Any troubleshooting done so far"
                },
                {
                    "text": "Timestamps"
                },
                {
                    "text": "Screenshots"
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---