<properties
    pageTitle="Problem with access denied (authorization)"
    description="Problem with access denied (authorization)"
    authors="davidmu1"
    ms.author="davidmu"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32689189,32689190"
    productPesIds="16952,16953,16954,16955,16956"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="1c56e5a9-eb1d-4ca8-874d-52b297d35199"
    	ownershipId="AzureIdentity_MSGraph"
/>

# Problem with access denied (authorization)

---
{
  "resourceRequired": false,
  "title": "Problem with access denied (authorization)",
  "fileAttachmentHint": "Provide a Fiddler/Charles proxy trace or HTTP request/responses",
  "subscriptionRequired": false,
  "formElements": [
    {
      "id": "request",
      "visibility": null,
      "order": 1,
      "controlType": "multilinetextbox",
      "displayLabel": "API request you are having a problem with",
      "content": null,
      "watermarkText": "Enter the Microsoft Graph REST call, or if using a client library enter the code snippet for the request that you are seeing an issue for.",
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
      "order": 2,
      "controlType": "multilinetextbox",
      "displayLabel": "Microsoft Graph error message",
      "content": null,
      "watermarkText": "Enter full API response error message",
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
      "order": 3,
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
          "value": "dont_know_answer",
          "text": "Other, don't know or not applicable"
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
      "order": 4,
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
      "order": 5,
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
      "order": 6,
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
      "order": 7,
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
      "order": 8,
      "controlType": "multilinetextbox",
      "displayLabel": "Symptoms of the problem",
      "content": null,
      "watermarkText": "Example: The /user API request is successful, but jobTitle and telephone number properties are missing",
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
      "order": 9,
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
      "order": 10,
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