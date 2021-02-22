<properties
	articleId="7FB68218-2D8E-4492-8DE0-8C5E7CD6E4FE"
	pageTitle="SQL Database"
	description="Scoping questions to capture driver related issues"
	authors="vitomaz-msft,MladjoA"
	authoralias="vitomaz"
	ms.author="vitomaz"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32745434,32745436"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_AzureSQLDB_Availability"
/>
# SQL Database
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": false,
    "resourceRequired": false,
    "title": "SQL Database",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },
        {
            "id": "sqlexception_received_on_client",
            "order": 20,
            "controlType": "multilinetextbox",
            "displayLabel": "Paste detailed error message or stack trace. (Obscure the personally identifiable information).",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide any additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ]
}
---