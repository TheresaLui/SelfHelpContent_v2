<properties
         pageTitle="Scoping questions for unable to configure or disable DB backup"
         description="Scoping questions for unable to configure or disable DB backup"
         authors="akanase-ot"
	     ms.author="akkanase"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32690768"
         productPesIds="15207"
         cloudEnvironments="public, fairfax, usnat, ussec"
         schemaVersion="1"
         articleId="0ce49c0d-bf98-4286-8788-44f77d9cdeab"
	ownershipId="StorageMediaEdge_Backup"
/>
# Questions unable to configure or disable DB backup
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "SAP HANA configuration failure",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "SAP HANA configuration failure",
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
            "displayLabel": "What is the SAP HANA version and edition?",
            "watermarkText": "ex. SAP HANA 2.0 SPS04",
            "required": false
        },
        {
            "id": "database_Name",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Provide the name(s) of the databases whose configuration is failing",
            "watermarkText": "Enter database name(s) separated by comma",
            "required": false
        },
        {
            "id": "sid_sap",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "Provide the SID for this SAP instance",
            "watermarkText": "Ex. HX1",
            "required": false
        },
        {
            "id": "jobID_Name",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "Enter the failed configuration job Activity ID",
            "watermarkText": "Ex. cace7461-dd3c-4e38-b4db-38dc57fdee7b",
            "required": false
        },
        {
            "id": "error_message",
            "order": 7,
            "controlType": "textbox",
            "displayLabel": "Provide the error message that you are seeing:",
            "watermarkText": "Copy and paste the error message details",
            "infoBalloonText": "Info: Please provide the error code that you are seeing in <a href='https://docs.microsoft.com/azure/backup/sap-hana-db-manage#view-backup-alerts'>Backup alerts</a>.",
            "required": false
        },
        {
            "id": "basic_troubleshooting_multiselect",
            "order": 8,
            "controlType": "multiselectdropdown",
            "infoBalloonText": "Info: <a href='https://docs.microsoft.com/azure/backup/sap-hana-backup-support-matrix#scenario-support'>Learn more</a> about the scenarios we support",
            "displayLabel": "Select the troubleshooting steps that you have performed:",
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
            "required": false,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "problem_description",
            "order": 10,
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
