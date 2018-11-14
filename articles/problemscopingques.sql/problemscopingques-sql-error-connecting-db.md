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
			"id": "problem_start_date",
			"order": 1,
			"controlType": "datetimepicker",
			"displayLabel": "Please enter the approximate time when the error was occurring (specify as your local time).",
			"required": true
		}, {
			"id": "error_dropdown",
			"order": 2,
			"controlType": "dropdown",
			"displayLabel": "What error were you seeing?",
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
			"id": "info_error_40613",
			"visibility": "error_dropdown == Error_40613",
			"order": 400,
			"controlType": "infoblock",
			"content": "Here is some sample text for error 40613.  We can add a hyperlink in here for common solutions"
		}, {
			"id": "activity_id",
			"visibility": "error_dropdown == Error_40613",
			"order": 401,
			"controlType": "textbox",
			"displayLabel": "Please provide the session tracing ID (only the GUID) from the text of the 40613 error message.",
			"required": false
		}, {
			"id": "info_login_timeout",
			"visibility": "error_dropdown == Error_Login_Timeout",
			"order": 700,
			"controlType": "infoblock",
			"displayLabel": "Please ensure you use a login timeout of at least 15 seconds.",
			"required": false
		}, {
			"id": "additional_details",
			"visibility": "error_dropdown == Error_Other",
			"order": 800,
			"controlType": "multilinetextbox",
			"displayLabel": "Please provide additional details",
			"required": false,
			"watermarkText": "Please describe in detail the issue you need assistance with.",
			"useAsAdditionalDetails": true,
			"hints": [{
					"text": "Always provide the error text from the underlying client library (e.g., SqlClient), as well as a client stack trace when the error occurred."
				}
			]
		}
	]
}
---
