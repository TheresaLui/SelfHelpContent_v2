<properties
    pageTitle="Problem with getting an access token (authentication)"
    description="Problem with getting an access token (authentication)"
    authors="davidmu1"
    ms.author="davidmu"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32689192"
    productPesIds="16952"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="a6dcd774-657f-4260-84ab-392c9c06c157"
    	ownershipId="AzureIdentity_MSGraph"
/>

# Problem with getting an access token (authentication)

---
{
  "resourceRequired": false,
  "title": "Problem with getting an access token (authentication)",
  "fileAttachmentHint": "Provide a Fiddler/Charles proxy trace or HTTP request/responses",
  "subscriptionRequired": false,
  "formElements": [
    {
      "id": "appTypeAndScenario",
      "visibility": null,
      "order": 1,
      "controlType": "dropdown",
      "displayLabel": "What app type and scenario are you using",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": "More details on app types and scenarios: https://docs.microsoft.com/azure/active-directory/develop/authentication-flows-app-scenarios.",
      "dropdownOptions": [
        {
          "text": "Single page applications (JavaScript) calling Microsoft Graph",
          "value": "SPA"
        },
        {
          "text": "Web application signing in a user and calling Microsoft Graph on behalf of the user",
          "value": "Web app"
        },
                {
          "text": "Web API calling Microsoft Graph on behalf of the signed-in user",
          "value": "Web API on behalf of"
        },
        {
          "text": "Desktop application calling Microsoft Graph on behalf of the signed-in user",
          "value": "Desktop"
        },
                {
          "text": "Mobile application calling Microsoft Graph on behalf of the user who's signed-in interactively",
          "value": "Mobile"
        },
        {
          "text": "Service daemon application calling Microsoft Graph on behalf of itself",
          "value": "Daemon"
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
      "id": "howAcquired",
      "visibility": null,
      "order": 2,
      "controlType": "dropdown",
      "displayLabel": "What are you using to get an access token?",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": "What library are you using to get an access token?",
      "dropdownOptions": [
        {
          "text": "Active Directory Authentication Library (ADAL)",
          "value": "ADAL"
        },
        {
          "text": "Microsoft Authentication Library (MSAL)",
          "value": "MSAL"
        },
        {
          "text": "Direct OAuth2.0 requests to the Azure AD v1.0 endpoint",
          "value": "Protocol-v1.0"
        },
        {
          "text": "Direct OAuth2.0 requests to the Azure AD v2.0 endpoint",
          "value": "Protocol-v2.0"
        },
        {
          "text": "Non-Microsoft OAuth2.0 library",
          "value": "Other-library"
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
      "id": "errorMessage",
      "visibility": null,
      "order": 3,
      "controlType": "multilinetextbox",
      "displayLabel": "Microsoft identity platform AADSTS error",
      "content": null,
      "watermarkText": "Enter the AADSTS* error code",
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "required": true,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 3
    },
    {
      "id": "hasErrorData",
      "visibility": null,
      "order": 4,
      "controlType": "dropdown",
      "displayLabel": "Do you have a correlation ID and a timestamp for the problematic request?",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": "Microsoft can provide a solution to your problem faster if you can provide a correlation ID and timestamp. You can find this info either in the HTTP response header or in the error response.",
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
      "id": "correlationId",
      "visibility": "hasErrorData==yes",
      "order": 5,
      "controlType": "textbox",
      "displayLabel": "Correlation ID",
      "content": null,
      "watermarkText": "Enter the correlation ID shown in the API response. This should be a GUID.",
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "required": false,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 0
    },
     {
            "id": "tenantID",
            "visibility": null,
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide target Tenant ID(s) (Comma separated, if multiple)",
            "content": null,
            "watermarkText": "Enter Tenant ID(s)",
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 2
        },
    {
      "id": "timestamp",
      "visibility": "hasErrorData==yes",
      "order": 7,
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
      "order": 8,
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
      "order": 9,
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
      "order": 10,
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
      "order": 11,
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
      "order": 12,
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
