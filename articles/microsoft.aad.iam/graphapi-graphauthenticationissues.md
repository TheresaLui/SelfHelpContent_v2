<properties
    pageTitle="Problem with grpah API authentication"
    description="graphauthenticationissues"
    authors="anupnadigm"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32134055"
    productPesIds="14785,16575"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    schemaVersion="1"
    articleID="9f90a783-6756-40a9-8231-b754e048c31f"
    	ownershipId="AzureIdentity_AppDevelopmentAndRegistration"
/>

# Problem with grpah API authentication

---
{
    "resourceRequired": false,
    "title": "Problem with grpah API authentication",
    "fileAttachmentHint": null,
    "formElements": [
        {
            "id": "errorMessage",
            "visibility": null,
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "Graph API request",
            "content": null,
            "watermarkText": "Enter the error message, including the correlation ID and timestamp. These values are either shown during sign-in or consent, or sent to the app during token acquistion.",
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "hints": [],
            "required": true,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 3
        },
        {
            "id": "whichUser",
            "visibility": null,
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Which user or admin is experiencing this problem?",
            "content": null,
            "watermarkText": "Enter user name or ID of the user in Azure Active Directory",
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
            "id": "tenantId",
            "visibility": "hasErrorData==no",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Tenant ID or tenant domain name",
            "content": null,
            "watermarkText": "Tenant ID or tenant domain that is experiencing the problem. Example: contoso.onmicrosoft.com OR tenant/organization id (GUID)",
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
            "id": "appId",
            "visibility": null,
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the Application name or Application ID experiencing this problem?",
            "content": null,
            "watermarkText": "Application ID is in the Properties section in the Azure AD configuration for the application",
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "hints": [],
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 2
        },
        {
            "id": "whatWasTheUserDoing",
            "visibility": null,
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "What was the user doing",
            "content": null,
            "watermarkText": "Example: Trying to sign-in, consent, trying to acquire a token.",
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "hints": [],
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 3
        },
        {
            "id": "problem_start_time",
            "visibility": null,
            "order": 6,
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
            "id": "problem_description",
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
    ],
    "$schema": "SelfHelpContent"
}
---