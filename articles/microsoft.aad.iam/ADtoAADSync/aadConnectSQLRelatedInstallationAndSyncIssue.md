<properties pageTitle = "Azure AD Connect issue with database" 
description = "Azure AD Connect issue with database" 
authors = "anmalath" 
selfHelpType = "aadConnectSQLRelatedInstallationAndSyncIssue" 
supportTopicIds = "32565592" 
productPesIds = "14785" 
cloudEnvironments = "public" 
schemaVersion = "1"/>

{
  "resourceRequired": true,
  "title": "Azure AD Connect issue with database",
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
      "id": "dBConfig",
      "visibility": "true",
      "order": 2,
      "controlType": "dropdown",
      "displayLabel": "What database is the Azure AD Connect server currently using?",
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
      "id": "problemDetails",
      "visibility": "true",
      "order": 3,
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
      "order": 4,
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
      "id": "filesToUpload",
      "visibility": "true",
      "order": 5,
      "controlType": "infoblock",
      "displayLabel": "Please provide a copy of the Windows Event logs (Application and System) during when the problem occurred. Put all the content to be shared into a single ZIP file and upload the file using 'File upload' on the left.",
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
      "id": "aadConnectSQLRelatedInstallationAndSyncIssueadditionalDetails",
      "visibility": null,
      "order": 6,
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