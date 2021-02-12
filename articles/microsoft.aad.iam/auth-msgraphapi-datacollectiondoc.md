<properties
    pageTitle="Problem with graph API generic"
    description="graphgenericapioperation"
    authors="anupnadigm"
    ms.author="anupnadigm"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32596860"
    productPesIds="16575"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    schemaVersion="1"
    articleId="df8b6aa7-fd87-40c7-8c0d-a67dd35aec46"
    ownershipId="AzureIdentity_DirectoryObjectManagement"
/>

# Problem with graph API generic

---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Problem with graph API generic",
    "fileAttachmentHint": null,
    "diagnosticCard": {
        "title": "Problem with Azure Active Directory app development with MSgraph",
        "description": "Please enter the following data for the self-service troubleshooter to assist in resolving your issue. Data can be retrieved from the Error Message or from the Azure Active Directory Sign-ins Blade:",
        "insightNotAvailableText": "Our troubleshooter did not detect any issues with your inputs."
    },
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
            "id": "problem_description",
            "visibility": null,
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Full Error Message:",
            "content": null,
            "watermarkText": "Example: AADSTS50076: Due to a configuration change made by your administrator...",
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "hints": null,
            "required": true,
            "maxLength": 0,
            "useAsAdditionalDetails": true,
            "numberOfLines": 3,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "correlationId",
            "visibility": null,
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Correlation ID:",
            "content": null,
            "watermarkText": "Example: 6ad36e38-8a10-4f1b-95fb-05cdb1dbec49",
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "requestId",
            "visibility": null,
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Request ID:",
            "content": null,
            "watermarkText": "Example: ca6161fb-000a-4d2f-a3b4-3d62168f866d",
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "hints": null,
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "timestamp",
            "visibility": null,
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "Date(UTC):",
            "content": null,
            "watermarkText": "Example: 2020-04-13T01:29:57.362Z",
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "hints": null,
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "symptoms",
            "visibility": null,
            "order": 6,
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
            "visibility": null,
            "order": 7,
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
            "visibility": null,
            "order": 8,
            "controlType": "textbox",
            "displayLabel": "Application ID",
            "content": null,
            "watermarkText": "Example: 751d4c55-15c1-4ed0-b2c0-ef30ebfe5743",
            "infoBalloonText": "Application to login to. Format accepted is AppID:751d4c55-15c1-4ed0-b2c0-ef30ebfe5743",
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
            "order": 9,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
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
        }
    ],
    "$schema": "SelfHelpContent"
}
---