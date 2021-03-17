<properties
	pageTitle="Error When Connecting to my Database"
	description="Scoping questions to capture more details about errors encountered while connecting to SQL DB"
	ms.author="msauthor"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="comma, seperated, list"
	productPesIds="productid"
	cloudEnvironments="public,blackForest,fairfax,mooncake"
	schemaVersion="1"
	articleId="newGuid"
	ownershipId="CloudES_AzureSupportPlatform"
/>
# Error When Connecting to my Database
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Error When Connecting to my Database",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "SQL DB Connectivity Troubleshooter",
        "description": "Our SQL DB Connectivity Troubleshooter can help you troubleshoot and solve your problem.",
        "insightNotAvailableText": "Our troubleshooter did not detect any issues with your resource. See our manual troubleshooting steps below to troubleshoot your problem."
    },
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "infoBalloonText": "Enter the approximate time you started to see the error.",
            "required": true,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "problem_end_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem stop? (If ongoing, leave this field blank)",
            "infoBalloonText": "Enter when the error stopped, or leave blank if the issue is ongoing.",
            "required": false,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "error_dropdown",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "What error are you seeing?",
            "watermarkText": "Choose an option",
            "infoBalloonText": "For other errors encountered during query execution, go back and select Problem Type = Performance and Query Execution",
            "dropdownOptions": [
                {
                    "value": "Error_Minus_1",
                    "text": "-1: A network-related or instance-specific error has occurred..."
                },
                {
                    "value": "Error_10928",
                    "text": "10928: The [request | session] limit for the database is [value] and has been reached"
                },
                {
                    "value": "Error_18456",
                    "text": "18456: Login failed for user [user name]"
                },
                {
                    "value": "Error_40613",
                    "text": "40613: Database [database name] on server [server name] is not currently available"
                },
                {
                    "value": "Error_40532_40615",
                    "text": "40532/40615: Cannot open server [server name] requested by the login"
                },
                {
                    "value": "Error_49918",
                    "text": "49918: Cannot process request. Not enough resources to process request"
                },
                {
                    "value": "Error_Login_Timeout",
                    "text": "Login/connection timeouts"
                },
                {
                    "value": "Error_Other",
                    "text": "Other error not listed"
                },
                {
                    "value": "dont_know_answer",
                    "text": "I don't know"
                }
            ],
            "required": true,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional context for the error message you are encountering.",
            "required": true,
            "useAsAdditionalDetails": true,
            "watermarkText": "Always provide the full error text from the underlying client library (e.g., SqlClient), not the general error from your client application.  If available, include the client stack trace as well."
        },
        {
		      "id": "sqlexception_received_on_client",
			    "order": 2000,
			    "controlType": "multilinetextbox",
    			"displayLabel": "Please provide the verbatim for the SQL error, or client error message you're seeing. Complete callstack (with appropriate user and/or application sensitive information redacted) is preferred.",
		    	"required": true,
			    "visibility": true
	    }
    ]
}
---
