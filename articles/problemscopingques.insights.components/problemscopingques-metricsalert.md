<properties
	articleId="problemscopingques-metricsalert"
	pageTitle="Metrics Alert"
	description="Metrics Alert"
	authors="debugthings"
	ms.author="jamdavi"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32613002"
	productPesIds="15693"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureMonitoring_ApplicationInsights"
/>
# Metrics Alert (Classic)
---
{
    "resourceRequired": true,
    "title": "Metrics Alert",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "classic_alert_id",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Please select the affected Metrics Alert resource.",
            "watermarkText": "Choose an option",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionid}/providers/microsoft.insights/metricAlerts?api-version=2018-03-01&%24filter=targetResource%20eq%20'%2Fsubscriptions%2F{subscriptionid}%2FresourceGroups%2F{resourcegroup}%2Fproviders%2Fmicrosoft.insights%2Fcomponents%2F{resourcename}'",
                "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$"
            },
            "dropdownOptions": [
                {
                    "value": "Unable to get the list of Alerts",
                    "text": "Unable to get the list of Alerts"
                }
            ],
            "required": false
        },
        {
            "id": "classic_alert_reason",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What is the primary issue with this alert rule?",
            "dropdownOptions": [
                {
                    "value": "Automation: Issues with REST API or Azure command line interface (CLI)",
                    "text": "Automation: Issues with REST API or Azure command line interface (CLI)"
                },
                {
                    "value": "Configuration: Creating, editing, or deleting alert rules",
                    "text": "Configuration: Creating, editing, or deleting alert rules"
                },
                {
                    "value": "Configuration: Issues with Azure resource manager (ARM) templates",
                    "text": "Configuration: Issues with Azure resource manager (ARM) templates"
                },
                {
                    "value": "Detection: Alert fires when it shouldn't",
                    "text": "Detection: Alert fires when it shouldn't"
                },
                {
                    "value": "Detection: Alert doesn’t fire when it should",
                    "text": "Detection: Alert doesn’t fire when it should"
                },
                {
                    "value": "Notifications: Not receiving notification from action group",
                    "text": "Notifications: Not receiving notification from action group"
                },
                {
                    "value": "Notifications: Unexpected content",
                    "text": "Notifications: Unexpected content"
                },
                {
                    "value": "Notifications: Delivered to unexpected set of recipients",
                    "text": "Notifications: Delivered to unexpected set of recipients"
                },
                {
                    "value": "General: Cannot view or find fired alerts",
                    "text": "General: Cannot view or find fired alerts"
                },
                {
                    "value": "General: Cannot view or find alert rule, action group, or another Azure resource",
                    "text": "General: Cannot view or find alert rule, action group, or another Azure resource"
                },
                {
                    "value": "General: Other issues",
                    "text": "General: Other issues"
                }
            ],
            "required": true
        },
        {
            "id": "affected_emails",
            "order": 3,
            "visibility": "classic_alert_reason == Notifications: Not receiving e-mail || classic_alert_reason == Notifications: Delivered to unexpected set of recipients",
            "watermarkText": "example1@example.com; example2@example.com",
            "infoBalloonText": "example1@example.com; example2@example.com",
            "controlType": "textbox",
            "displayLabel": "Please enter a semi-colon delimited list of e-mail addresses that are affected by this problem",
            "required": true
        },
        {
            "id": "action_group",
            "order": 4,
            "visibility": "classic_alert_reason == Notifications: Not receiving notification from action group || classic_alert_reason == Notifications: Delivered to unexpected set of recipients",
            "controlType": "dropdown",
            "displayLabel": "Please select the affected Action Group.",
            "watermarkText": "Choose an option",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionid}/providers/microsoft.insights/actionGroups?api-version=2017-04-01",
                "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$"
            },
            "dropdownOptions": [
                {
                    "value": "Unable to get the list of Action Groups",
                    "text": "Unable to get the list of Action Groups"
                }
            ],
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide these details",
            "required": true,
            "watermarkText": "Please provide: a detailed scenario of the error condition, troubleshooting done so far, log files, timestamp, screenshots, and any other relevant information.",
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Expected behavior, actual behavior"
                },
                {
                    "text": "Troubleshooting done so far"
                },
                {
                    "text": "Log Files"
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
