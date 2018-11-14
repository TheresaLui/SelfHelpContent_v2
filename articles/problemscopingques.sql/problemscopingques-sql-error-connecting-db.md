<properties
	pageTitle="Error When Connecting to my Database"
	description="Scoping questions to capture more details about errors encountered while connecting to SQL DB"
	authors="keithelm"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32628800"
	productPesIds="13491"
	cloudEnvironments="Public"
	schemaVersion="1"
/>
# Error When Connecting to my Database
---
{
	"resourceRequired": false,
	"title": "Error When Connecting to my Database",
	"fileAttachmentHint": "",
	"formElements": [{
			"id": "error_selection",
			"order": 1,
			"controlType": "DropDown",
			"displayLabel": "Please select the error message you need assistance with.",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "-1: A network-related or instance-specific error has occurred...",
					"text": "Error_Minus_1"
				}, {
					"value": "10928: The session limit for the database is X and has been reached",
					"text": "Error_10928"
				}, {
					"value": "18456: Login failed for user X",
					"text": "Error_18456"
				}, {
					"value": "40613: Database X on server Y is not currently available",
					"text": "Error_40613"
				}, {
					"value": "40615: Cannot open server X requested by the login",
					"text": "Error_40615"
				}, {
					"value": "Login/connection timeouts",
					"text": "Error_Login_Timeout"
				}, {
					"value": "Other error not listed ",
					"text": "Error_Other"
				}
			],
			"required": true
		}, {
			"id": "problem_start_date",
			"order": 2,
			"controlType": "datetimepicker",
			"displayLabel": "Please select the approximate time when the error was occurring, specified as UTC.",
			"required": true
		}, {
			"id": "activity_id",
			"visibility": "error_selection == Error_40613"
			"order": 10,
			"controlType": "TextBox",
			"displayLabel": "Please provide the session tracing ID (only the GUID) from the text of the 40613 error message.",
			"required": false
		}, {
			"id": "additional_details",
			"visibility": "error_selection == Error_Other"
			"order": 11,
			"controlType": "multilinetextbox",
			"displayLabel": "Please provide additional details",
			"required": false,
			"useAsAdditionalDetails": true,
			"hints": [{
					"text": "Issue description."
				}, {
					"text": "Please provide the error text from the underlying client library (e.g., SqlClient), as well as a client stack trace when the error occurred."
				}
			]
		}
	]
}
---
