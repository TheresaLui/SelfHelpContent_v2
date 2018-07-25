<properties pageTitle="Conditional Access issue" 
	 description="Conditional Access issue" 
	 authors="anupnadigm" 
	 selfHelpType="appsconditionalaccessdatacollectiondoc" 
	 supportTopicIds="32570276,32596842,32596872,32596859,32596896,32596903" 
	 productPesIds="14785" 
	 cloudEnvironments="public" 
	 schemaVersion="1"
/> 
# Conditional Access issue 
---
{
  "resourceRequired": true,
  "title": "Conditional Access issue",
  "fileAttachmentHint": "Screenshot of problem",
  "formElements": [
    {
      "id": "whichUser",
      "visibility": null,
      "order": 1,
      "controlType": "textbox",
      "displayLabel": "Who is the user who is having the problem?",
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
      "id": "task",
      "visibility": null,
      "order": 2,
      "controlType": "multilinetextbox",
      "displayLabel": "What is the user trying to accomplish?",
      "content": null,
      "watermarkText": "Examples: trying to create a conditional access policy, trying to sign in to an application",
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
      "order": 3,
      "controlType": "multilinetextbox",
      "displayLabel": "What are the symptoms of the failure?",
      "content": null,
      "watermarkText": "Examples: user sign in was unexpectedly blocked by conditional access",
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
      "id": "hasErrorData",
      "visibility": null,
      "order": 5,
      "controlType": "dropdown",
      "displayLabel": "Do you have correlation ID for this problem?",
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
      "id": "correlationId",
      "visibility": "hasErrorData==yes",
      "order": 6,
      "controlType": "textbox",
      "displayLabel": "Correlation ID",
      "content": null,
      "watermarkText": "Enter the correlation ID that was shown when the user attempted to sign in.",
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
      "id": "correlationIdTimestamp",
      "visibility": "hasErrorData==yes",
      "order": 7,
      "controlType": "textbox",
      "displayLabel": "Timestamp",
      "content": null,
      "watermarkText": "Enter the Timestamp that was shown when the user attempted to sign in.",
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
      "id": "getCorrelationId",
      "visibility": "hasErrorData!=yes",
      "order": 8,
      "controlType": "infoblock",
      "displayLabel": "If the user is getting blocked during sign in, collect the correlation ID and timestamp from they are shown under ''More details'''.'",
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
      "id": "appsConditionalAccessDataCollectionDocadditionalDetails",
      "visibility": null,
      "order": 9,
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
---