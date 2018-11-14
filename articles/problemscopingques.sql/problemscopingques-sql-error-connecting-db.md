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
			"id": "problem_start_time",
			"order": 1,
			"controlType": "datetimepicker",
			"displayLabel": "Please enter the approximate time when the error started occurring.",
			"required": true
		}, {
			"id": "problem_end_time",
			"order": 2,
			"controlType": "datetimepicker",
			"displayLabel": "Please enter the approximate time when the error stopped occurring. If the issue is ongoing, leave this field blank.",
			"required": false
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
					"text": "10928: Resource ID: X. The Y limit for the database is Z and has been reached"
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
			"id": "info_error_10928",
			"visibility": "error_dropdown == Error_10928",
			"order": 100,
			"controlType": "infoblock",
			"content": "The Resource ID value in this error indicates which resource governance limit is being hit.  A value of 1 is a limit on worker threads; 2 indicates a limit on sessions (connections) to the database.  Either increase the <a href='https://docs.microsoft.com/azure/sql-database/sql-database-service-tiers-dtu'>service tier</a> of your database, or tune the workload so that it fits within your selected tier.  Refer to the <a href='https://docs.microsoft.com/azure/sql-database/sql-database-query-performance'>Query Performance Insight</a> feature for assistance analyzing and tuning your workload."
		}, {
			"id": "info_error_18456",
			"visibility": "error_dropdown == Error_18456",
			"order": 200,
			"controlType": "infoblock",
			"content": "Troubleshoot this error using the <a href='https://support.microsoft.com/help/10085/troubleshooting-connectivity-issues-with-microsoft-azure-sql-database '>Azure SQL Database troubleshooter</a>."
		}, {
			"id": "info_error_40613",
			"visibility": "error_dropdown == Error_40613",
			"order": 400,
			"controlType": "infoblock",
			"content": "This common, transient error occurs when you database is undergoing a reconfiguration, and normally lasts less than 60 seconds.  <a href='https://docs.microsoft.com/azure/sql-database/sql-database-troubleshoot-common-connection-issues'>Read more</a> about how to handle this."
		},{
			"id": "info_error_40615",
			"visibility": "error_dropdown == Error_40615",
			"order": 500,
			"controlType": "infoblock",
			"content": "To resolve this error, please create a server firewall rule as described <a href='https://docs.microsoft.com/azure/sql-database/sql-database-vnet-service-endpoint-rule-overview#errors-40914-and-40615'>here</a>."
		}, {
			"id": "info_login_timeout",
			"visibility": "error_dropdown == Error_Login_Timeout",
			"order": 700,
			"controlType": "infoblock",
			"content": "Ensure your application is using a login timeout of at least 15 seconds.  Also confirm that the database is not hitting the <a href='https://docs.microsoft.com/azure/sql-database/sql-database-service-tiers-dtu'>limits</a> of your selected service tier."
		}, {
			"id": "error_details",
			"order": 1000,
			"controlType": "multilinetextbox",
			"displayLabel": "Please provide additional context for the error message you are encountering.",
			"required": true,
			"watermarkText": "Always provide the full error text from the underlying client library (e.g., SqlClient), not the general error from your client application.  If available, include the client stack trace as well.",
			"useAsAdditionalDetails": true
		}
	]
}
---
