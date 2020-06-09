<properties
    pageTitle="Problem using Microsoft Graph samples, Graph Explorer, or getting started"
    description="Problem using Microsoft Graph samples, Graph Explorer, or getting started"
    authors="davidmu1"
    ms.author="davidmu"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32689194"
    productPesIds="16953,16954,16955,16956"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="17bc8a89-5623-4a01-9c6f-579fe9189f04"
    	ownershipId="AzureIdentity_GraphUsersAndGroupsAPIs"
/>

# Problem using Microsoft Graph samples, Graph Explorer, or getting started

---
{
  "resourceRequired": false,
  "title": "Problem using Microsoft Graph samples, Graph Explorer or getting started",
  "fileAttachmentHint": "Provide a Fiddler/Charles proxy trace or HTTP request/responses",
  "subscriptionRequired": false,
  "formElements": [
    {
      "id": "sampleExplorerOrGettingStarted",
      "visibility": null,
      "order": 1,
      "controlType": "dropdown",
      "displayLabel": "Which of Microsoft Graph samples, Graph Explorer or Quick Start/Tutorials are you having issues with?",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": "Pick from Microsoft Graph samples, Microsoft Graph Explorer or Quick Start/Tutorials.",
      "dropdownOptions": [
        {
          "text": "Microsoft Graph samples",
          "value": "samples"
        },
        {
          "text": "Microsoft Graph Explorer",
          "value": "explorer"
        },
        {
          "text": "Quick Start/Tutorials",
          "value": "gettingStarted"
        },
        {
          "text": "Don't know answer",
          "value": "dont_know_answer"
        }
      ],
      "dynamicDropdownOptions": null,
      "required": true,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 0
    },
    {
      "id": "samples",
      "visibility": "sampleExplorerOrGettingStarted==samples",
      "order": 2,
      "controlType": "multilinetextbox",
      "displayLabel": "Which sample are you having problems with?",
      "content": null,
      "watermarkText": "Enter a link to the sample GitHub repo",
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "required": true,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 2
    },
    {
      "id": "gettingStarted",
      "visibility": "sampleExplorerOrGettingStarted==gettingStarted",
      "order": 3,
      "controlType": "multilinetextbox",
      "displayLabel": "Which quick start or tutorial are you having problems with?",
      "content": null,
      "watermarkText": "Enter a link to the quick start or the tutorial",
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "required": true,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 2
    },
    {
      "id": "codeRequest",
      "visibility": "sampleExplorerOrGettingStarted==samples",
      "order": 4,
      "controlType": "multilinetextbox",
      "displayLabel": "Code snippet or REST request you are having a problem with",
      "content": null,
      "watermarkText": "Enter the code snippet or REST call for the request you are seeing an issue with",
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "required": true,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 3
    },
    {
      "id": "errorMessage",
      "visibility": null,
      "order": 5,
      "controlType": "multilinetextbox",
      "displayLabel": "Microsoft Graph error message",
      "content": null,
      "watermarkText": "Enter full error response message (if you have one)",
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "required": false,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 3
    },
    {
      "id": "hasErrorData",
      "visibility": null,
      "order": 6,
      "controlType": "dropdown",
      "displayLabel": "Do you have a client request ID and a timestamp for the problematic request?",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": "Microsoft can provide a solution to your problem faster if you can provide a client request ID and timestamp. You can find this info either in the HTTP response header or in the error response.",
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
          "text": "Don't know answer",
          "value": "dont_know_answer"
        }
      ],
      "dynamicDropdownOptions": null,
      "required": true,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 0
    },
    {
      "id": "requestId",
      "visibility": "hasErrorData==yes",
      "order": 7,
      "controlType": "textbox",
      "displayLabel": "Client request ID",
      "content": null,
      "watermarkText": "Enter the client request ID shown in the API response. This should be a GUID.",
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "required": false,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 0
    },
    {
      "id": "timestamp",
      "visibility": "hasErrorData==yes",
      "order": 8,
      "controlType": "textbox",
      "displayLabel": "Timestamp",
      "content": null,
      "watermarkText": "Enter the timestamp shown in the API response.",
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "required": false,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 0
    },
    {
      "id": "tenantId",
      "visibility": "hasErrorData==no",
      "order": 9,
      "controlType": "textbox",
      "displayLabel": "Tenant ID or tenant domain name",
      "content": null,
      "watermarkText": "Tenant ID or tenant domain that is experiencing the problem. Example: contoso.onmicrosoft.com OR tenant/organization id (GUID)",
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "required": false,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 0
    },
    {
      "id": "appId",
      "visibility": "hasErrorData==no",
      "order": 10,
      "controlType": "textbox",
      "displayLabel": "Application ID",
      "content": null,
      "watermarkText": "App ID of the application that is experiencing the problem",
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "required": false,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 0
    },
    {
      "id": "symptoms",
      "visibility": "hasErrorData==no",
      "order": 11,
      "controlType": "multilinetextbox",
      "displayLabel": "Symptoms of the problem",
      "content": null,
      "watermarkText": "Example: The request to Users is successful, but jobTitle and telephone number properties are null",
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "required": false,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 3
    },
    {
      "id": "problem_start_time",
      "visibility": null,
      "order": 12,
      "controlType": "datetimepicker",
      "displayLabel": "When did the problem begin?",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "required": false,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 0
    },
    {
      "id": "problem_description",
      "visibility": null,
      "order": 13,
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
  ],
  "$schema": "SelfHelpContent"
}
---