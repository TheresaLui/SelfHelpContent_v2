<properties
	pageTitle="Error When Connecting to my Database"
	description="Scoping questions to capture more details about errors encountered while connecting to SQL DB"
	authors="keithelm"
	ms.author="keithelm,muruga,emlisa"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630423"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake"
	schemaVersion="1"
	articleId="1688B2F2-D77C-4D1D-BDBF-928FA372704C"
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
            "id": "problem_description",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional context for the error message you are encountering.",
            "required": true,
            "useAsAdditionalDetails": true,
            "watermarkText": "Always provide the full error text from the underlying client library (e.g., SqlClient), not the general error from your client application.  If available, include the client stack trace as well."
        },
        {
                "id": "sqlexception_received_on_client",
                "order": 3,
                "controlType": "multilinetextbox",
                "displayLabel": "Please provide the verbatim for the SQL error, or client error message you're seeing.              Complete callstack (with appropriate user and/or application sensitive information redacted) is preferred.",
                "required": true,
                "visibility": true
        },
        {
            "id": "database_name",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Please provide the database name for which you are creating a support ticket.",
            "required": true,
            "infoBalloonText": "Which of these databases are you filing a ticket for?",
            "dynamicDropdownOptions": {
                        "uri": "{servername}/databases?api-version=2017-10-01-preview",
                        "jTokenPath": "value",
                        "textProperty": "properties.description",
                        "valueProperty": "id",
                        "textPropertyRegex": null,
                        "defaultDropdownOptions": {
                                        "value": "dont_know_answer",
                                        "text": "Don't know/None of these"
                                    }
            }
        }
    ]
}
---
