<properties
         pageTitle="Scoping questions for unable to discover VM"
         description="Scoping questions for unable to discover VM"
         authors="srinathvasireddy"
	 ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32632804"
         productPesIds="15207"
         cloudEnvironments="public, fairfax, usnat, ussec"
         schemaVersion="1"
         articleId="9e3ebca0-af2a-4446-ad72-98ea62a6bce2"
	ownershipId="StorageMediaEdge_Backup"
/>
# Questions for unable to discover VM
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Unable to discover VM",
    "fileAttachmentHint": "",
      "diagnosticCard": {
        "title": "Unable to discover VM",
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
            "id": "error_message",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Provide the error message if you are seeing:",
            "watermarkText": "Copy and paste the error message details",
            "required": false
        },
        {
            "id": "basic_troubleshooting_multiselect",
            "order": 5,
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
            "order": 6,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 7,
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
