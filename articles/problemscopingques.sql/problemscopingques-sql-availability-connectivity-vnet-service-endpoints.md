<properties
	pageTitle="Resource Health Scoping Questions"
	description="Scoping questions to capture more details about Availability and Connectivity\Resource Health support topic"
	authors="keithelm"
	ms.author="keithelm,muruga,emlisa"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630460"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake"
	schemaVersion="1"
	articleId="112AA2F8-EE65-4414-8308-4E3F43C54152"
/>
# Scoping questions for VNet Service Endpoints
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Resource Health Scoping Questions",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "Unavailability start time",
            "infoBalloonText": "Please provide the start time of the most recent occurence of unavailability.",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional context to help us solve your issue.",
            "required": true,
            "useAsAdditionalDetails": true,
            "watermarkText": "On the Basics tab, please ensure you selected a server, database or elastic pool in the Resource dropdown so we know what resource you need assistance with.  Add any additional details that may help us troubleshoot your issue."
        },
        {
            "id": "sqlexception_received_on_client",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide the verbatim for the SQL error, or client error message you're seeing.Complete          callstack (with appropriate user and/or application sensitive information redacted) is preferred.",
            "required": false,
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
