<properties
	articleId="problemscopingques-sql-createdropresources-firewallrules"
	pageTitle="SQL Database"
	description="Scoping questions to capture CRUD issues for firewall rules"
	authors="andikshi"
	authoralias="andikshi"
	ms.author="andikshi"
	selfHelpType="problemScopingQuestions"
	productPesIds="13491"
	supportTopicIds="32630421"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_AzureSQLDB_Provisioning"
/>
# SQL Database
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": false,
    "title": "Database",
    "fileAttachmentHint": "",
    "subscriptionRequired": false,
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controltype": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "watermarkText": "Specify when the problem started",
            "infoBalloonText": "Specify when the problem started",
            "required": true
        },
	{
            "id": "rule_type",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What type of firewall rule you are configuring",
            "required": true,
            "dropdownOptions": [
                {
                    "value": "server",
                    "text": "Server level firewall rule"
                },
                {
                    "value": "database",
                    "text": "Database level firewall rule"
                },
                {
                    "text": "Other, don't know or not applicable",
                    "value": "dont_know_answer"
                }
            ]
        },
	{
            "id": "issue_type",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "What issue are you facing with firewall rules?",
            "required": true,
            "dropdownOptions": [
                {
                    "value": "adding_rule",
                    "text": "Adding a firewall rule?"
                },
                {
                    "value": "removing_rule",
                    "text": "Removing a firewall rule?"
                },
                {
                    "text": "Other, don't know or not applicable",
                    "value": "dont_know_answer"
                }
            ]
        },
        {
            "id": "attempt_method",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "What method are you using",
            "required": true,
            "dropdownOptions": [
                {
                    "value": "azure_portal",
                    "text": "Azure Portal"
                },
		{
                    "value": "t-sql",
                    "text": "Transact-SQL"
                },
                {
                    "value": "powershell",
                    "text": "Powershell"
                },
                {
                    "value": "azure_cli",
                    "text": "Azure CLI"
                },
  		{
                    "value": "rest_api",
                    "text": "REST API"
                },
                {
                    "text": "Other, don't know or not applicable",
                    "value": "dont_know_answer"
                }
            ]
        },
        {
            "id": "encountering_an_error",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Are you encountering an error message?",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Unsure"
                }
            ],
            "required": false
        },
        {
            "id": "error_message",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide the error message",
            "required": false,
            "visibility": "encountering_an_error == Yes"
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
