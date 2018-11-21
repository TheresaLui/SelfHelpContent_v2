<properties
	pageTitle="Metrics Alert (Classic)"
	description="Metrics Alert (Classic)"
	authors="debugthings"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32613002"
	productPesIds="15693"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="problemscopingques-classicalert"
/>
# Metrics Alert (Classic)
---
{
	"resourceRequired": true,
	"title": "Metrics Alert (Classic)",
	"fileAttachmentHint": "",
	"formElements": [{
			"id": "classic_alert_id",
			"order": 1,
			"controlType": "dropdown",
			"displayLabel": "Please select the affected Metrics Alert (Classic) resource name.",
			"watermarkText": "Choose an option",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionid}/resourceGroups/{resourcegroup}/resources?api-version=2018-09-01&$filter=resourcetype eq'microsoft.insights%2Falertrules'",
                "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$"
            },
			"dropdownOptions": [{
					"value": "Unable to get the list of Alerts",
					"text": "Unable to get the list of Alerts"
				}],
			"required": false
		}, {
			"id": "classic_alert_reason",
			"order": 2,
			"controlType": "dropdown",
			"displayLabel": "What is the primary issue with this alert rule?",
			"dropdownOptions": [
				{
					"value": "Automation: Issues with REST API or Azure command line interface (CLI)",
					"text": "Automation: Issues with REST API or Azure command line interface (CLI)"
				},{
					"value": "Configuration: Creating, editing or deleting alert rules",
					"text": "Configuration: Creating, editing or deleting alert rules"
				}, {
					"value": "Configuration: Issues with Azure resource manager (ARM) templates",
					"text": "Configuration: Issues with Azure resource manager (ARM) templates"
				}, {
					"value": "Detection: Alert fires when it should NOT",
					"text": "Detection: Alert fires when it should NOT"
				}, {
					"value": "Detection: Alert doesn’t fire when it should",
					"text": "Detection: Alert doesn’t fire when it should"
				}, {
					"value": "Notifications: Not receiving web hook",
					"text": "Notifications: Not receiving web hook"
				}, {
					"value": "Notifications: Not receiving e-mail",
					"text": "Notifications: Not receiving e-mail"
				}, {
					"value": "Notifications: Receiving with delay",
					"text": "Notifications: Receiving with delay"
				}, {
					"value": "Notifications: Unexpected content",
					"text": "Notifications: Unexpected content"
				}, {
					"value": "Notifications: Delivered to unexpected set of recipients",
					"text": "Notifications: Delivered to unexpected set of recipients"
				}, {
					"value": "General: Cannot view or find fired alerts",
					"text": "General: Cannot view or find fired alerts"
				}, {
					"value": "General: Cannot view or find alert rule, action group or another Azure resource",
					"text": "General: Cannot view or find alert rule, action group or another Azure resource"
				}, {
					"value": "General: Other issues",
					"text": "General: Other issues"
				}],
			"required": true
		}, {
			"id": "affected_emails",
			"order": 3,
			"visibility": "classic_alert_reason == Notifications: Not receiving e-mail || classic_alert_reason == Notifications: Delivered to unexpected set of recipients",
			"watermarkText": "example1@example.com; example2@example.com",
			"infoBalloonText": "example1@example.com; example2@example.com",
			"controlType": "textbox",
			"displayLabel": "Please enter a semi-colon delimited list of e-mail addresses that are affected by this problem",
			"required": true
		},{
			"id": "problem_start_time",
			"order": 4,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true
		},{
			"id": "problem_description",
			"order": 5,
			"controlType": "multilinetextbox",
			"displayLabel": "Please provide these details",
			"required": true,
			"watermarkText": "Please provide: a detailed scenario of the error condition, troubleshooting done so far, log files, timestamp, screenshots and any other relevant information.",
			"useAsAdditionalDetails": true,
			"hints": [{
					"text": "Detailed scenario of the error condition"
				}, {
					"text": "Troubleshooting done so far and how you determined this is incorrect behavior"
				}, {
					"text": "Log Files"
				}, {
					"text": "Timestamps"
				}, {
					"text": "Screenshots"
				}

			]
		}
	]
}
---