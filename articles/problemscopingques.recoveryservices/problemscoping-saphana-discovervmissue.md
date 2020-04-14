<properties
         pageTitle="Scoping questions for unable to discover VM"
         description="Scoping questions for unable to discover VM"
         authors="akanase-ot"
         ms.author="akkanase"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32690769"
         productPesIds="15207"
         cloudEnvironments="public, fairfax, usnat, ussec"
         schemaVersion="1"
         articleId="75b25de5-3e57-44a7-bf88-0e6a4a569208"
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
      "id": "sap_version",
      "order": 3,
      "controlType": "textbox",
      "displayLabel": "What is the SAP HANA version and edition?",
      "watermarkText": "ex. SAP HANA 2.0 SPS04",
      "required": false
    },
    {
      "id": "error_message",
      "order": 4,
      "controlType": "textbox",
      "displayLabel": "Provide the error message if you are seeing:",
      "watermarkText": "Copy and paste the error message details",
      "infoBalloonText": "Info: Please provide the error code that you are seeing in <a href='https://docs.microsoft.com/azure/backup/sap-hana-db-manage#view-backup-alerts'>Backup alerts</a>.",
      "required": false
    },
    {
      "id": "basic_troubleshooting_multiselect",
      "order": 5,
      "controlType": "multiselectdropdown",
      "infoBalloonText": "Info: <a href='https://docs.microsoft.com/azure/backup/sap-hana-backup-support-matrix#scenario-support'>Learn more</a> about the scenarios we supports",
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
      "required": false,
      "diagnosticInputRequiredClients": "Portal"
    },
    {
      "id": "problem_start_time",
      "order": 6,
      "controlType": "datetimepicker",
      "displayLabel": "When did the problem begin?",
      "required": false
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
