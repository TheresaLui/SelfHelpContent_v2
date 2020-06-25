<properties
         pageTitle="Scoping questions for SAP HANA restore failure"
         description="Scoping questions for SAP HANA restore failure"
         authors="akanase-ot"
         ms.author="akkanase"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32690772"
         productPesIds="15207"
         cloudEnvironments="public, fairfax, usnat, ussec"
         schemaVersion="1"
         articleId="cc2bea57-b728-43a9-a8e1-317dfd55ab07"
	ownershipId="StorageMediaEdge_Backup"
/>
# Questions SAP HANA restore failure
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "SAP HANA restore failure",
    "fileAttachmentHint": "",
    "diagnosticCard": {
       "title": "SAP HANA restore failure",
       "description": "These diagnostics will check for errors.",
       "insightNotAvailableText": "We didn't find any problems"
    },
    "formElements": [
        {
            "id": "machine_name",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Which machine is experiencing the problem?",
            "watermarkText": "Select the virtual machine running SAP HANA",
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
            "id": "desired_target",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "In case of Alternate location restore, are you able to see the desired target machine?",
            "watermarkText": "Select",
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
                    "text": "Other, don't know or not applicable"
                }
            ]
        },
        {
            "id": "database_Name",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Provide the name(s) of the databases whose restore is failing?",
            "watermarkText": "Enter database name(s) comma separated",
            "required": false
        },
        {
            "id": "restore_Type",
            "order": 4,
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
            "required": false,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "restore_Type1",
            "order": 5,
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
            "required": false,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "error_message",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "Provide the error message that are you seeing:",
            "watermarkText": "Example: UserErrorHanaUnsupportedOperation",
            "infoBalloonText": "Info: Please provide the error code that you are seeing in <a href='https://docs.microsoft.com/azure/backup/sap-hana-db-manage#view-backup-alerts'>Backup alerts</a>.",
            "required": false
        },
        {
            "id": "jobID_Name",
            "order": 7,
            "controlType": "textbox",
            "displayLabel": "Enter the failed restore job Activity ID:",
            "watermarkText": "Ex. cace7461-dd3c-4e38-b4db-38dc57fdee7b",
            "required": false
        },
        {
            "id": "basic_troubleshooting_multiselect",
            "order": 8,
            "controlType": "multiselectdropdown",
            "infoBalloonText": "Info: <a href='https://docs.microsoft.com/azure/backup/sap-hana-backup-support-matrix#scenario-support'>Learn more</a> about the scenarios we support",
            "displayLabel": "Select the troubleshooting steps you have performed:",
            "dropdownOptions": [
                {
                    "value": "Checked OS version is supported for backup",
                    "text": "Checked OS version is supported for backup"
                },
                {
                    "value": "Checked SAP HANA version and edition are supported for backup",
                    "text": "Checked SAP HANA version and edition are supported for backup"
                },
                {
                    "value": "Checked the Machine has Internet connectivity",
                    "text": "Checked the Machine has Internet connectivity"
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
            "required": false
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
