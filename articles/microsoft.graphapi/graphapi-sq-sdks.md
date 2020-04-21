<properties
    pageTitle="Problem using the Microsoft Graph SDK or libraries"
    description="Problem using the Microsoft Graph SDK or libraries"
    authors="davidmu1"
    ms.author="davidmu"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32689195"
    productPesIds="16953,16954,16955,16956"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="115e4513-d6db-436f-9820-8b5f4436b715"
    	ownershipId="AzureIdentity_GraphUsersAndGroupsAPIs"
/>

# Problem using the Microsoft Graph SDK or libraries

---
{
  "resourceRequired": false,
  "title": "Problem using the Microsoft Graph SDK or libraries",
  "fileAttachmentHint": "Provide a Fiddler/Charles proxy trace or HTTP request/responses",
  "subscriptionRequired": false,
  "formElements": [
      {
      "id": "whichLangOrPlatform",
      "visibility": null,
      "order": 1,
      "controlType": "dropdown",
      "displayLabel": "What language/platform are you using?",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": "More details on supported languages and platforms: https://docs.microsoft.com/graph/sdks/sdks-overview.",
      "dropdownOptions": [
        {
          "text": "Android",
          "value": "Android"
        },
        {
          "text": "Angular",
          "value": "Angular"
        },
        {
          "text": "ASP.NET",
          "value": "ASP.NET"
        },
        {
          "text": "iOS",
          "value": "iOS"
        },
        {
          "text": "Javascript",
          "value": "Javascript"
        },
        {
          "text": "Node.js",
          "value": "Node.js"
        },
        {
          "text": "Java",
          "value": "Java"
        },
        {
          "text": "PHP",
          "value": "PHP"
        },
        {
          "text": "Python",
          "value": "Python"
        },
        {
          "text": "Ruby",
          "value": "Ruby"
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
      "id": "request",
      "visibility": null,
      "order": 2,
      "controlType": "multilinetextbox",
      "displayLabel": "Code you are having a problem with",
      "content": null,
      "watermarkText": "Enter the code snippet for the request that you are seeing an issue with",
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
      "order": 3,
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
      "order": 4,
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
      "order": 5,
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
      "order": 6,
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
      "order": 7,
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
      "order": 8,
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
      "order": 9,
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
      "order": 10,
      "controlType": "datetimepicker",
      "displayLabel": "When did the problem begin?",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "required": true,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 0
    },
    {
      "id": "problem_description",
      "visibility": null,
      "order": 11,
      "controlType": "multilinetextbox",
      "displayLabel": "Please provide additional details",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "required": true,
      "maxLength": 0,
      "useAsAdditionalDetails": true,
      "numberOfLines": 0
    }
  ],
  "$schema": "SelfHelpContent"
}
---