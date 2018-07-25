<properties pageTitle = "Active Directory application access panel issue" 
description = "Active Directory application access panel issue" 
authors = "anmalath" 
selfHelpType = "appsAccessPanelDataCollectionDoc" 
supportTopicIds = "32570265" 
productPesIds = "14785" 
cloudEnvironments = "public" 
schemaVersion = "1"/>

{
  "resourceRequired": true,
  "title": "Active Directory application access panel issue",
  "fileAttachmentHint": null,
  "formElements": [
    {
      "id": "whichUser",
      "visibility": null,
      "order": 1,
      "controlType": "textbox",
      "displayLabel": "Which user or admin is experiencing this problem?",
      "content": null,
      "watermarkText": "Enter user name or Object ID of the user in Azure Active Directory",
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
      "id": "problem",
      "visibility": null,
      "order": 2,
      "controlType": "multilinetextbox",
      "displayLabel": "What is the user or admin trying to accomplish?",
      "content": null,
      "watermarkText": "Examples: trying to access an application, trying to register for MFA / SSPR , trying to sign in to an application.",
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": null,
      "required": true,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 2
    },
    {
      "id": "whereProblem",
      "visibility": null,
      "order": 3,
      "controlType": "multilinetextbox",
      "displayLabel": "Where is the user or admin trying to accomplish this task?",
      "content": null,
      "watermarkText": "Examples: in the Access Panel, in the Office 365 Portal, signing-in to an application deeplink",
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": null,
      "required": true,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 2
    },
    {
      "id": "symptoms",
      "visibility": null,
      "order": 4,
      "controlType": "multilinetextbox",
      "displayLabel": "What are the symptoms of the problem?",
      "content": null,
      "watermarkText": "Examples: error message in the Access Panel, error message on signing in, error message in the Office 365 portal",
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": null,
      "required": true,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 2
    },
    {
      "id": "whichApp",
      "visibility": null,
      "order": 5,
      "controlType": "multilinetextbox",
      "displayLabel": "Which application is the problem related to?",
      "content": null,
      "watermarkText": "If the problem is with a specific application, enter its display name or object ID here. Or enter 'All apps' or 'Not applicable', if appropriate.",
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": null,
      "required": true,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 2
    },
    {
      "id": "appsAccessPanelDataCollectionDocadditionalDetails",
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