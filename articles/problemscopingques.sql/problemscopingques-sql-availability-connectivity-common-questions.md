<properties
	pageTitle="Resource Health Scoping Questions"
	description="Scoping questions to capture more details about Availability and Connectivity\Resource Health support topic"
	authors="keithelm"
	ms.author="keithelm,muruga,emlisa,swbhartims"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630414, 32630423, 32630460"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake"
	schemaVersion="1"
	articleId="217152B3-3A59-4441-8B67-B20B2DE5CD95"
/>
# Scoping questions for Configure or use Azure Active Directory authentication
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": true,
    "subscriptionRequired": true,
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
            "displayLabel": "Please provide the verbatim for the SQL error, or client error message you're seeing.              Complete callstack (with appropriate user and/or application sensitive information redacted) is preferred.",
            "required": false,
            "visibility": true
        },
        {
            "id": "database_name",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Please provide the database name for which you are creating a support ticket. If multiple databases are affected, select one of the affected databases to start an investigation",
            "required": false,
            "infoBalloonText": "Which of these databases are you filing a ticket for?",
            "dynamicDropdownOptions": {
                        "uri": "{resourceId}/databases?api-version=2017-10-01-preview",
                        "jTokenPath": "value",
                        "textProperty": "name",
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
