<properties pageTitle = "Active Directory application proxy issue" 
description = "Active Directory application proxy issue" 
authors = "anmalath" 
selfHelpType = "appsAppProxyDataCollectionDoc" 
supportTopicIds = "32369657,32570275" 
productPesIds = "14785" 
cloudEnvironments = "public" 
schemaVersion = "1"/>

{
  "resourceRequired": true,
  "title": "Active Directory application proxy issue",
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
      "watermarkText": "Examples: add a connector to a connector group, enable access to an on-premises app, sign in to an application.",
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
      "watermarkText": "Examples: in the Azure portal, on the 'All applications' page in Enterprise Applications; PowerShell; signing in to an on-premises application",
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
      "watermarkText": "Examples: error message in the Azure portal, error message on signing in, incorrect data on application properties page",
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
      "id": "appsAppProxyDataCollectionDocadditionalDetails",
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