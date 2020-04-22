<properties
         pageTitle="Scoping questions for unable to discover DB"
         description="Scoping questions for unable to discover DB"
         authors="srinathvasireddy"
	 ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32632803"
         productPesIds="15207"
         cloudEnvironments="public, fairfax, usnat, ussec"
         schemaVersion="1"
         articleId="aa4dd4bc-49b1-4de7-a5ea-caceaa1b3563"
	ownershipId="StorageMediaEdge_Backup"
/>
# Questions for unable to discover DB
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Unable to discover DB",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "Unable to discover DB",
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
            "required": false,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "database_Name",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Provide the name(s) of the databases you are unable to discover:",
            "watermarkText": "Enter database name(s) separated by comma",
            "required": false
        },
        {
            "id": "error_message",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "Provide the error message if you are seeing:",
            "watermarkText": "Copy and paste the error message details",
            "required": false
        },
        {
            "id": "basic_troubleshooting_multiselect",
            "order": 6,
            "controlType": "multiselectdropdown",
            "infoBalloonText": "Check the SQL database backup <a href='https://aka.ms/AB-AA4dp5m'>supported scenario</a>",
            "displayLabel": "Select the troubleshooting steps that you have performed:",
            "dropdownOptions": [
                {
                    "value": "Checked OS version is supported for backup",
                    "text": "Checked OS version is supported for backup"
                },
                {
                    "value": "Checked SQL version and edition are supported for backup",
                    "text": "Checked SQL version and edition are supported for backup"
                },
                {
                    "value": "Checked the Machine has Internet connectivity",
                    "text": "Checked the Machine has Internet connectivity"
                },
                {
                    "value": "Checked the SQL Server VM has required permission for backup",
                    "text": "Checked the SQL Server VM has required permission for backup"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "problem_start_time",
            "order": 7,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 8,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details:",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "hints": []
        }
    ],
    "$schema": "SelfHelpContent"
}
---
