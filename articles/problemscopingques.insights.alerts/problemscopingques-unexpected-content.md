<properties
	articleId="problemscopingques-unexpected-content"
	pageTitle="Notification content is not what I expected"
	description="Notification content is not what I expected"
	authors="snehithm"
	ms.author="snmuvva"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32629652, 32629665, 32629666, 32629667, 32629668, 32629670"
	productPesIds="15454"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureMonitoring_ActionGroup"
/>
# Notification content is not what I expected
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Notification content is not what I expected",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "notification_type",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Which type of notification has this problem?",
            "watermarkText": "Choose a notification type",
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