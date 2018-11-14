<properties
	pageTitle="Error When Connecting to my Database"
	description="Scoping questions to capture more details about errors encountered while connecting to SQL DB"
	authors="keithelm"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32628800"
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
	"formElements": [{
			"id": "error_selection",
			"order": 1,
			"controlType": "dropdown",
			"displayLabel": "Please select the error message you need assistance with.",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Error_Minus_1",
					"text": "-1: A network-related or instance-specific error has occurred..."
				}, {
					"value": "Error_10928",
					"text": "10928: The session limit for the database is X and has been reached"
				}, {
					"value": "Error_18456",
					"text": "18456: Login failed for user X"
				}, {
					"value": "Error_40613",
					"text": "40613: Database X on server Y is not currently available"
				}, {
					"value": "Error_40615",
					"text": "40615: Cannot open server X requested by the login"
				}, {
					"value": "Error_Login_Timeout",
					"text": "Login/connection timeouts"
				}, {
					"value": "Error_Other",
					"text": "Other error not listed"
				}
			],
			"required": true
		}, {
			"id": "problem_start_date",
			"order": 2,
			"controlType": "datetimepicker",
			"displayLabel": "Please select the approximate time when the error was occurring (specified as your local time).",
			"required": true
		}, {
			"id": "activity_id",
			"order": 10,
			"controlType": "textbox",
			"displayLabel": "Please provide the session tracing ID (only the GUID) from the text of the 40613 error message.",
			"required": false
		}, {
			"id": "additional_details",
			"visibility": "error_selection == Other error not listed"
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
