<properties pageTitle = "Problem in Identity Protection users risk events" 
description = "Problem in Identity Protection users risk events" 
authors = "anmalath" 
selfHelpType = "identityProtection" 
supportTopicIds = "32542231" 
productPesIds = "14785" 
cloudEnvironments = "public" 
schemaVersion = "1"/>

{
  "resourceRequired": true,
  "title": "Problem in Identity Protection users risk events",
  "fileAttachmentHint": null,
  "formElements": [
    {
      "id": "ProblemAreas",
      "visibility": null,
      "order": 1,
      "controlType": "dropdown",
      "displayLabel": "Problem Areas",
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
      "id": "symptoms",
      "visibility": null,
      "order": 2,
      "controlType": "multilinetextbox",
      "displayLabel": "What are the symptoms of the problem?",
      "content": null,
      "watermarkText": null,
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
      "id": "ObjectIDs",
      "visibility": "ProblemAreas==riskyUsers",
      "order": 3,
      "controlType": "multilinetextbox",
      "displayLabel": "Object IDs of impacted users",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": null,
      "required": false,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 1
    },
    {
      "id": "whenBegan",
      "visibility": null,
      "order": 4,
      "controlType": "datetimepicker",
      "displayLabel": "When did the problem begin?",
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
      "id": "VulnerabilityType",
      "visibility": "ProblemAreas==Vulnerabilities",
      "order": 5,
      "controlType": "dropdown",
      "displayLabel": "Vulnerability type",
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
      "id": "riskEventType",
      "visibility": "ProblemAreas==riskEvents",
      "order": 6,
      "controlType": "dropdown",
      "displayLabel": "Risk event type",
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
      "id": "identityProtectionadditionalDetails",
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