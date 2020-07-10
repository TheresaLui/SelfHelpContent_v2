<properties
    pageTitle="Problem with graph API generic"
    description="graphgenericapioperation"
    authors="anupnadigm"
    ms.author="anupnadigm"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32596839,32596841,32596852,32134056"
    productPesIds="16578,16575"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    schemaVersion="1"
    articleId="7a7a3d35-6f8b-4f79-8b95-ef0c1f5709e4"
    	ownershipId="AzureIdentity_DirectoryObjectManagement"
/>

# Problem with graph API generic

---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Problem with graph API generic",
    "fileAttachmentHint": null,
    "formElements": [
        {
            "id": "request",
            "visibility": null,
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "Graph API request for which you are seeing the problem",
            "content": null,
            "watermarkText": "Enter the Azure AD or Microsoft Graph REST call, or if using a client library enter the code snippet for the request that you are seeing an issue for.",
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
            "id": "errorMessage",
            "visibility": null,
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Graph API error message",
            "content": null,
            "watermarkText": "Enter an API response error message (if you have one)",
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "hints": null,
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
            "displayLabel": "Do you have a client request ID and a timestamp for the error related to this problem?",
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
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "dynamicDropdownOptions": null,
            "hints": null,
            "required": true,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "getData",
            "visibility": "hasErrorData!=yes",
            "order": 4,
            "controlType": "infoblock",
            "displayLabel": null,
            "content": "Microsoft can provide a solution to your problem faster if you can provide a client request ID and timestamp. You can find this info either in the HTTP response header or in the error response.",
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
            "hints": null,
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
            "hints": null,
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "symptoms",
            "visibility": "hasErrorData==no",
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "Symptoms of the problem",
            "content": null,
            "watermarkText": "Example: The /user API request is successful, but jobTitle and telephone number properties are missing",
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "hints": null,
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 3
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
            "hints": null,
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
            "hints": null,
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
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
            "hints": null,
            "required": false,
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