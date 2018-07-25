<properties pageTitle = "AAD Connect Synchronization - Other questions" 
description = "AAD Connect Synchronization - Other questions" 
authors = "anmalath" 
selfHelpType = "aadConnectOtherQuestionsRegardingActiveDirectoryToAzureADSynchronization" 
supportTopicIds = "32404465" 
productPesIds = "14785" 
cloudEnvironments = "public" 
schemaVersion = "1"/>

{
  "resourceRequired": true,
  "title": "AAD Connect Synchronization - Other questions",
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
      "watermarkText": "Please describe the problem you have, including symptoms and errors encountered.",
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
      "id": "aadConnectOtherQuestionsRegardingActiveDirectoryToAzureADSynchronizationadditionalDetails",
      "visibility": null,
      "order": 4,
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