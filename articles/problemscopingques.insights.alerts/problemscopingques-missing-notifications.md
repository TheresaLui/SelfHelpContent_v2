<properties
	articleId="problemscopingques-missing-notifications"
	pageTitle="Not receiving notifications"
	description="Not receiving notifications"
	authors="snehithm"
	ms.author="snmuvva"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32629650, 32629653, 32629654, 32629655, 32629656, 32629658"
	productPesIds="15454"
	cloudEnvironments="public, Fairfax"
	schemaVersion="1"
	ownershipId="AzureMonitoring_ActionGroup"
/>
# Not receiving notifications
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Not receiving notifications",
    "fileAttachmentHint": "Provide screenshots of alert rule you are not receiving notifications for",
    "formElements": [
        {
            "id": "notification_type",
            "order": 1,
            "controlType": "multiselectdropdown",
            "displayLabel": "Which type of notifications are you not receiving?",
            "watermarkText": "Choose one or more notification types",
            "dropdownOptions": [
                {
                    "value": "Email",
                    "text": "Email"
                },
                {
                    "value": "SMS",
                    "text": "SMS"
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
                },
                {
                    "value": "ITSM",
                    "text": "ITSM"
                },
                {
                    "value": "Phone call",
                    "text": "Voice/Phone call"
                }
            ],
            "required": false
        },
        {
            "id": "action_group_id",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Please select the affected action group resource",
            "watermarkText": "Choose an action group",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionid}/providers/microsoft.insights/actionGroups?api-version=2017-04-01",
                "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$"
            },
            "dropdownOptions": [
                {
                    "value": "Unable to get the list of Action groups",
                    "text": "Unable to get the list of Action groups"
                }
            ],
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 4,
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