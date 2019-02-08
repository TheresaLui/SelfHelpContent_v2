<properties
	pageTitle="Error When Connecting to my Database"
	description="Scoping questions to capture more details about errors encountered while connecting to SQL DB"
	authors="keithelm"
	ms.author="keithelm,muruga,emlisa"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630429"
	productPesIds="13491"
	cloudEnvironments="Public"
	schemaVersion="1"
	articleId="D748D991-21A6-4FBD-B98E-7962F6100F9A"
/>
# Error When Connecting to my Database
---
{
	"resourceRequired": false,
	"title": "Error When Connecting to my Database",
	"fileAttachmentHint": "",
	"diagnosticCard": {
		"title": "SQL DB Connectivity Troubleshooter",
    		"description": "Our SQL DB Connectivity Troubleshooter can help you troubleshoot and solve your problem.",
    		"insightNotAvailableText": "We didn't find any insights"
	},
"formElements": [{
			"id": "problem_start_time",
			"order": 1,
			"controlType": "datetimepicker",
			"displayLabel": "Please enter the approximate time when the error started occurring.",
			"required": true,
			"diagnosticInputRequiredClients": "Portal"
		}, {
			"id": "problem_end_time",
			"order": 2,
			"controlType": "datetimepicker",
			"displayLabel": "Please enter the approximate time when the error stopped occurring. If the issue is ongoing, leave this field blank.",
			"required": false,
			"diagnosticInputRequiredClients": "Portal"
		}, {
			"id": "error_dropdown",
			"order": 5,
			"controlType": "dropdown",
			"displayLabel": "What error are you seeing?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Error_Minus_1",
					"text": "-1: A network-related or instance-specific error has occurred..."
				}, {
					"value": "Error_10928",
					"text": "10928: Resource ID: [id]. The [resource type] limit for the database is [value] and has been reached"
				}, {
					"value": "Error_18456",
					"text": "18456: Login failed for user [user name]"
				}, {
					"value": "Error_40613",
					"text": "40613: Database [database name] on server [server name] is not currently available"
				}, {
					"value": "Error_40615",
					"text": "40615: Cannot open server [server name] requested by the login"
				}, {
					"value": "Error_Login_Timeout",
					"text": "Login/connection timeouts"
				}, {
					"value": "Error_Other",
					"text": "Other error not listed"
				}
			],
			"required": true,
			"diagnosticInputRequiredClients": "Portal"
		}, {
			"id": "problem_description",
			"order": 1000,
			"controlType": "multilinetextbox",
			"displayLabel": "Please provide additional context for the error message you are encountering.",
			"required": true,
			"useAsAdditionalDetails": true,
			"watermarkText": "Always provide the full error text from the underlying client library (e.g., SqlClient), not the general error from your client application.  If available, include the client stack trace as well."
		}
	]
}
---
