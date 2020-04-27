<properties
	articleId="problemscopingques-alert-delay"
	pageTitle="Receiving notifications with delay"
	description="Receiving notifications with delay"
	authors="snehithm"
	ms.author="snmuvva"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32629651, 32629659, 32629660, 32629661, 32629662, 32629664"
	productPesIds="15454"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureMonitoring_ActionGroup"
/>
# Notifications received with delay
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Issues with notification delays",
    "fileAttachmentHint": "Provide notifications that you received with delay",
    "formElements": [
        {
            "id": "delay_type",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "How did you determine there was a delay?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Fired alert appears in portal with delay",
                    "text": "Fired alert appears in portal with delay"
                },
                {
                    "value": "Receiving notifications (email, webhook etc.) with delay",
                    "text": "Receiving notifications (email, webhook etc.) with delay"
                }
            ],
            "required": false
        },
        {
            "id": "action_group_id",
            "order": 2,
            "visibility": "delay_type == Receiving notifications (email, webhook etc.) with delay",
            "controlType": "dropdown",
            "displayLabel": "Please select action group that is sending the delayed notifications",
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