<properties
         pageTitle="Scoping questions for SQL database backup failure"
         description="Scoping questions for SQL database backup failure"
         authors="srinathv"
         ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32605791"
         productPesIds="15207"
         cloudEnvironments="public"
         schemaVersion="1"
         articleId="d73dbe86-4f8e-414d-8963-7d22d012b671"
/>
# Questions SQL database backup failure
---
{
    "resourceRequired": true,
    "title": "SQL database backup failure",
    "fileAttachmentHint": "",
    "formElements": [
        {
        "id": "machine_name",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Which machine is experiencing the problem?",
            "watermarkText": "Select the virtual machine running SQL",
            "dynamicDropdownOptions": {
        "uri": "/subscriptions/{subscriptionid}/providers/Microsoft.Compute/virtualMachines?api-version=2018-05-01&$filter=resourceType eq 'Microsoft.Compute/virtualMachines' or resourceType eq 'Microsoft.ClassicCompute/virtualMachines'",
        "jTokenPath": "value",
        "textProperty": "name",
        "valueProperty": "id",
        "textPropertyRegex": ".*"
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
            "displayLabel": "Provide the name(s) of the databases whose backup is failing?",
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
            "displayLabel": "Select the troubleshooting steps you have performed:",
            "dropdownOptions": [
                {
                    "value": "OS version is supported for backup",
                    "text": "OS version is supported for backup"
                },
                {
                    "value": "SQL version and edition are supported for backup",
                    "text": "SQL version and edition are supported for backup"
                },
                {
                    "value": "Machine has Internet connectivity",
                    "text": "Machine has Internet connectivity"
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
            "required": true
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
    ]
}
---
