<properties pageTitle = "Azure AD Connect synchronization issue with specific attribute" 
description = "Azure AD Connect synchronization issue with specific attribute" 
authors = "anmalath" 
selfHelpType = "aadConnectSynchronizationProblemForASpecificAttribute" 
supportTopicIds = "32565590" 
productPesIds = "14785" 
cloudEnvironments = "public" 
schemaVersion = "1"/>

{
  "resourceRequired": true,
  "title": "Azure AD Connect synchronization issue with specific attribute",
  "fileAttachmentHint": "Upload the ZIP file",
  "formElements": [
    {
      "id": "aadConnector",
      "visibility": "true",
      "order": 1,
      "controlType": "multilinetextbox",
      "displayLabel": "Azure AD Connect version",
      "content": null,
      "watermarkText": "Please specify the Azure AD Connect version you have. For example, 1.1.552.0.",
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": null,
      "required": true,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 1
    },
    {
      "id": "problemDetails",
      "visibility": "true",
      "order": 2,
      "controlType": "multilinetextbox",
      "displayLabel": "What is the problem?",
      "content": null,
      "watermarkText": "Please describe the problem you have, including symptoms and errors encountered. If you have received notification of synchronization error for this issue, please paste the error details and include the TrackingId (if available).",
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": null,
      "required": true,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 3
    },
    {
      "id": "whenOccurred",
      "visibility": null,
      "order": 3,
      "controlType": "datetimepicker",
      "displayLabel": "When did the problem occur?",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": null,
      "required": false,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 0
    },
    {
      "id": "whatTriggeredTheIssue",
      "visibility": "true",
      "order": 4,
      "controlType": "dropdown",
      "displayLabel": "Is the problem caused by one of the following changes?",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": null,
      "required": true,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 0
    },
    {
      "id": "askForSetupLogs",
      "visibility": "whatTriggeredTheIssue==configChangeInWizard",
      "order": 5,
      "controlType": "infoblock",
      "displayLabel": "Please share the setup logs. If the Azure AD Connect version is 1.1.443.0 or after, the logs are located under '%programdata%\\AADConnect'. Otherwise, they are located under '%localappdata%\\AADConnect'. Please share provide the entire folder.",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": null,
      "required": false,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 0
    },
    {
      "id": "askForSyncRules",
      "visibility": "whatTriggeredTheIssue==syncRuleChange",
      "order": 6,
      "controlType": "infoblock",
      "displayLabel": "Please run cmdlet Get-ADSyncRule and save the output to a text file. Put all the content to be shared into a single ZIP file and upload the file using 'File upload' on the left.",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": null,
      "required": false,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 0
    },
    {
      "id": "aadConnectSynchronizationProblemForASpecificAttributeadditionalDetails",
      "visibility": null,
      "order": 7,
      "controlType": "multilinetextbox",
      "displayLabel": "Please provide additional details",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": null,
      "required": true,
      "maxLength": 0,
      "useAsAdditionalDetails": true,
      "numberOfLines": 0
    }
  ]
}