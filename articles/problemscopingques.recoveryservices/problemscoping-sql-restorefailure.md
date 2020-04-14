<properties
         pageTitle="Scoping questions for SQL database restore failure"
         description="Scoping questions for SQL database restore failure"
         authors="srinathvasireddy"
	 ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32605795"
         productPesIds="15207"
         cloudEnvironments="public, fairfax, usnat, ussec"
         schemaVersion="1"
         articleId="7937a50e-344f-4502-856b-b8d23dd8d99a"
	ownershipId="StorageMediaEdge_Backup"
/>
# Questions SQL database restore failure
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "SQL database restore failure",
    "fileAttachmentHint": "",
    "diagnosticCard": {
       "title": "SQL database restore failure",
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
            "id": "database_Name",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Provide the name(s) of the databases whose restore is failing?",
            "watermarkText": "Enter database name(s) comma separated",
            "required": false
        },
        {
            "id": "restore_Type",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Which type of restore are you performing?",
            "watermarkText": "Select",
            "dropdownOptions": [
                {
                    "value": "Alternate Location",
                    "text": "Alternate Location"
                },
                {
                    "value": "Overwrite DB",
                    "text": "Overwrite DB"
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
            "id": "restore_Type1",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Are you performing Logs (Point in Time)/Full & Differential restoration?",
            "watermarkText": "Select",
            "dropdownOptions": [
                {
                    "value": "Logs (Point in Time)",
                    "text": "Logs (Point in Time)"
                },
                {
                    "value": "Full & Differential",
                    "text": "Full & Differential"
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
            "id": "jobID_Name",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "Enter the failed restore job Activity ID:",
            "watermarkText": "Ex. cace7461-dd3c-4e38-b4db-38dc57fdee7b",
            "required": false
        },
        {
            "id": "error_code",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "Provide the error code that are you seeing:",
            "watermarkText": "Example: UserErrorSQLPODoesNotExist",
            "required": false
        },
        {
            "id": "basic_troubleshooting_multiselect",
            "order": 7,
            "controlType": "multiselectdropdown",
            "displayLabel": "Select the troubleshooting steps you have performed:",
            "dropdownOptions": [
                {
                    "value": "OS version is supported for resotre",
                    "text": "OS version is supported for restore"
                },
                {
                    "value": "SQL version and edition are supported for restore",
                    "text": "SQL version and edition are supported for restore"
                },
                {
                    "value": "Machine has Internet connectivity",
                    "text": "Machine has Internet connectivity"
                },
                {
                    "value": "SQL server VM has required permission for restore",
                    "text": "SQL server VM has required permission for restore"
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
            "order": 8,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 9,
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
