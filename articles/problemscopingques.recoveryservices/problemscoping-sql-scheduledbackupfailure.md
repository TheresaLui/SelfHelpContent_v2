<properties
         pageTitle="Scoping questions for SQL database scheduled backup failure"
         description="Scoping questions for SQL database scheduled backup failure"
         authors="srinathv"
         ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32632801"
         productPesIds="15207"
         cloudEnvironments="public, fairfax, usnat, ussec"
         schemaVersion="1"
         articleId="b7e6ce67-6f7f-487a-9841-021943d0af57"
	ownershipId="StorageMediaEdge_Backup"
/>
# Questions SQL database scheduled backup failure
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "SQL database scheduled backup failure",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "SQL database scheduled backup failure",
        "description": "These diagnostics will check for errors.",
        "insightNotAvailableText": "We didn't find any problems"
    },
    "formElements": [
        {
        "id": "machine_name",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Which machine is experiencing the problem?",
            "watermarkText": "Select the virtual machine running SQL",
            "dynamicDropdownOptions": {
        "uri": "/subscriptions/{subscriptionid}/resources?api-version=2018-05-01&$filter=resourceType eq 'Microsoft.Compute/virtualMachines' or resourceType eq 'Microsoft.ClassicCompute/virtualMachines'",
        "jTokenPath": "value",
        "textProperty": "name",
        "valueProperty": "id",
        "textPropertyRegex": ".*",
	"defaultDropdownOptions": {
                           "value": "dont_know_answer",
                           "text": "Other or none of the above"
                     }
       },
     "required": false
     },
        {
            "id": "os_version",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "What is the OS version of the machine?",
            "watermarkText": "ex. Windows Server 2012 R2",
            "required": false
        },
        {
            "id": "sql_version",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What is the SQL Server version and edition?",
            "watermarkText": "ex. SQL Server 2012 Standard",
            "required": false
        },
        {
            "id": "database_Name",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Provide the name(s) of the databases whose scheduled backup is failing?",
            "watermarkText": "Enter database name(s) comma separated",
            "required": false
        },
        {
            "id": "backup_Type",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Is the failure happening during Full/Log/Differential backup?",
            "watermarkText": "Select",
            "dropdownOptions": [
                {
                    "value": "Full backup",
                    "text": "Full backup"
                },
                {
                    "value": "Log backup",
                    "text": "Log backup"
                },
                {
                    "value": "Differential backup",
                    "text": "Differential backup"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": false
        },
        {
            "id": "jobID_Name",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "Enter the failed backup job Activity ID",
            "watermarkText": "Ex. cace7461-dd3c-4e38-b4db-38dc57fdee7b",
            "required": false
        },
        {
            "id": "error_code",
            "order": 7,
            "controlType": "textbox",
            "displayLabel": "Provide the error code that are you seeing:",
            "watermarkText": "Example: UserErrorSQLPODoesNotExist",
            "required": false
        },
        {
            "id": "basic_troubleshooting_multiselect",
            "order": 8,
            "controlType": "multiselectdropdown",
            "infoBalloonText": "Check <a href='https://aka.ms/AA4dqho'>pre-requisites</a>, <a href='https://aka.ms/AB-AA4dp5t'>network requirements</a> articles",
            "displayLabel": "Select the troubleshooting steps you have performed:",
            "dropdownOptions": [
                {
                    "value": "Machine has Internet connectivity",
                    "text": "Machine has Internet connectivity"
                },
                {
                    "value": "NSG/Proxy is configured and required URLs are whitelisted",
                    "text": "NSG/Proxy is configured and required URLs are whitelisted"
                },
                {
                    "value": "SQL server VM has required permission for backup",
                    "text": "SQL server VM has required permission for backup"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 9,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true,
     "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "problem_description",
            "order": 10,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "hints": []
        }
    ],
    "$schema": "SelfHelpContent"
}
---
