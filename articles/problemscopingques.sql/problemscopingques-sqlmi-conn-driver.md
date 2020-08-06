<properties
	articleId="problemscopingques-sqlmi-conn-connectiontimeouts"
	pageTitle="SQL Database Managed Instance"
	description="Scoping questions to capture driver related issues"
	authors="vitomaz-msft,MladjoA"
	authoralias="vitomaz"
	ms.author="vitomaz"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32637245,32637247,32637259"
	productPesIds="16259"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_AzureSQLMI"
/>
# SQL Database Managed Instance
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": false,
    "resourceRequired": false,
    "title": "SQL Database Managed Instance",
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
            "id": "driver_name",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Driver or tool you are experiencing issues with?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": ".NET Framework",
                    "text": ".NET Framework"
                },
                {
                    "value": "ODBC driver",
                    "text": "ODBC driver"
                },
                {
                    "value": "PHP driver",
                    "text": "PHP driver"
                },
                {
                    "value": "JDBC driver",
                    "text": "JDBC driver"
                },
                {
                    "value": "Node.js driver",
                    "text": "Node.js driver"
                },
                {
                    "value": "OLEDB driver",
                    "text": "OLEDB driver"
                },
                {
                    "value": "SSMS",
                    "text": "SSMS"
                },
                {
                    "value": "SMO",
                    "text": "SMO"
                },
                {
                    "text": "Other, don't know or not applicable",
                    "value": "dont_know_answer"
                }
            ],
            "required": false
        },
        {
            "id": "driver_version",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Version of the driver or tool?",
            "watermarkText": "Provide the version of your driver/tool",
            "required": false,
            "useAsAdditionalDetails": false
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
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ]
}
---