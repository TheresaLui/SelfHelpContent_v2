<properties
    pageTitle="Multi-Factor Authentication"
    description="Bot Insight with Scoping Questing for MFA"
    authors="jameswang"
    ms.author="yixwang"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32615515,32615519,32739619,32739617,32739616"
    productPesIds="16579"
    cloudEnvironments="public, fairfax,  Mooncake, usnat, ussec"
    schemaVersion="1"
    articleId="Multifactor_Authentication_BOT_No_DSQ"
    ownershipId="AzureIdentity_MultiFactorAuthentication"
/>

# Active Directory application single sign on issue

---
{
    "resourceRequired": false,
	"subscriptionRequired": false,
    "title": "Active Directory application single sign on issue",
    "fileAttachmentHint": null,
    "formElements": [
        {
            "id": "VerboseTracing",
            "visibility": null,
            "order": 1,
            "controlType": "infoblock",
            "displayLabel": null,
            "content": "Before requesting support, Microsoft suggests you enable advanced diagnostics that will gather more information about your problem.",
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
            "id": "enableVerboseTracing1",
            "visibility": null,
            "order": 2,
            "controlType": "infoblock",
            "displayLabel": null,
            "content": "To enable advance diagnosis:",
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
            "id": "enableVerboseTracing2",
            "visibility": null,
            "order": 3,
            "controlType": "infoblock",
            "displayLabel": null,
            "content": "Open a new browser tab and paste https://login.microsoftonline.com/common/debugmode/enable?user={username} (replace {username} with the upn of the user in question; eg: user=johndoe@contoso.com) and then try to reproduce the error.",
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
            "order": 4,
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
            "numberOfLines": 3
        },
        {
            "id": "correlationId",
            "visibility": null,
            "order": 5,
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
            "numberOfLines": 0
        },
        {
            "id": "requestId",
            "visibility": null,
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "Request ID:",
            "content": null,
            "watermarkText": "Example: ca6161fb-000a-4d2f-a3b4-3d62168f866d",
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
            "visibility": "null",
            "order": 7,
            "controlType": "textbox",
            "displayLabel": "Date(UTC):",
            "content": null,
            "watermarkText": "Example: 2020-04-13T01:29:57.362Z",
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "appNameOrId",
            "visibility": "null",
            "order": 8,
            "controlType": "multilinetextbox",
            "displayLabel": "Application name or ID:",
            "content": null,
            "watermarkText": "Example: ContosoApp",
            "infoBalloonText": "Application to login to. Format accepted is App Name:ContosoApp or AppID:751d4c55-15c1-4ed0-b2c0-ef30ebfe5743",
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 2
        },
        {
            "id": "userNameOrId",
            "visibility": "null",
            "order": 9,
            "controlType": "textbox",
            "displayLabel": "User Experiencing Problem:",
            "content": null,
            "watermarkText": "Example: foo@contoso.com",
            "infoBalloonText": "User who made the sign-in request. Format accepted is UPN:foo@contoso.com  or ObjectID:224ad664-d4a8-41fc-9ddf-121db97fa120",
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "problem_start_time",
            "order": 10,
            "controlType": "datetimepicker",
            "displayLabel": "Problem start time",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
