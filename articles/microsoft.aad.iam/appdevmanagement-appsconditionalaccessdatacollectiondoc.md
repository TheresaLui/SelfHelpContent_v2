<properties
    pageTitle="Conditional Access issue"
    description="appsconditionalaccessdatacollectiondoc"
    authors="anupnadigm"
    selfHelpType="problemScopingQuestions"
    supportTopicIds=""
    productPesIds=""
    cloudEnvironments="public"
    schemaVersion="1"
    articleId="17f35c58-24cd-4be7-b90f-fe6f7b64def5"
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
      "hints": [],
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
      "hints": [],
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
      "hints": [],
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
      "hints": [],
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
      "dropdownOptions": [
        {
          "text": "Yes",
          "value": "yes"
        },
        {
          "text": "No",
          "value": "no"
        },
        {
          "text": "Other, don't know or not applicable",
          "value": "other"
        }
      ],
      "dynamicDropdownOptions": null,
      "hints": [],
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
      "hints": [],
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
      "hints": [],
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
      "displayLabel": null,
      "content": "If the user is getting blocked during sign in, collect the correlation ID and timestamp from they are shown under ''More details'''.'",
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": [],
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