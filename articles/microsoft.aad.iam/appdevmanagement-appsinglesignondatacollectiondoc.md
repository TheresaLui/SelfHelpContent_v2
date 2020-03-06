<properties
    pageTitle="Active Directory application single sign on issue"
    description="appsinglesignondatacollectiondoc"
    authors="hsku"
	ms.author="hsku"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32570259"
    productPesIds="16575"
    cloudEnvironments="public"
    schemaVersion="1"
    articleId="appsinglesignondatacollectiondoc"
    	ownershipId="AzureIdentity_EnterpriseApps"
/>

# Active Directory application single sign on issue

---
{
    "resourceRequired": false,
	"subscriptionRequired": false,
    "title": "Active Directory application single sign on issue",
    "fileAttachmentHint": null,
    "diagnosticCard": {
        "title": "Problem with Azure Active Directory application single sign",
        "description": "Our self-service troubleshooter can help you troubleshoot and solve your problem.",
        "insightNotAvailableText": "Our troubleshooter did not detect any issues with your inputs."
    },
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
            "id": "hasErrorData",
            "visibility": null,
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Do you have a correlation ID and Timestamp for an error related to this problem?",
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
                }
            ],
            "dynamicDropdownOptions": null,
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "getCorrelationId",
            "visibility": "hasErrorData==no",
            "order": 5,
            "controlType": "infoblock",
            "displayLabel": null,
            "content": "Microsoft can provide a solution to your problem faster if you can get a correlation ID and Timestamp for this problem, reproduce the error by signing into the app with your own account.",
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
            "id": "correlationId",
            "visibility": "hasErrorData==yes",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "Correlation ID from Error message:",
            "content": null,
            "watermarkText": "Copy the correlation ID from the error message and paste it here",
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
            "id": "timestamp",
            "visibility": "hasErrorData==yes || hasErrorData==no",
            "order": 7,
            "controlType": "textbox",
            "displayLabel": "Timestamp from Error message:",
            "content": null,
            "watermarkText": "Copy the timestamp from the error message and paste it here",
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
            "id": "appNameOrId",
            "visibility": "null",
            "order": 8,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the Application name or Application ID experiencing this problem?",
            "content": null,
            "watermarkText": "Application ID is in the Properties section in the Azure AD configuration for the application",
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 2,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "userNameOrId",
            "visibility": "hasErrorData==no",
            "order": 9,
            "controlType": "textbox",
            "displayLabel": "Which user is experiencing this problem?",
            "content": null,
            "watermarkText": "Enter user upn or Object ID of the user in Azure Active Directory",
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
            "id": "problem_description",
            "visibility": null,
            "order": 10,
            "controlType": "multilinetextbox",
            "displayLabel": "If you received an error, please provide the error message details:",
            "content": null,
            "watermarkText": "AADSTSXXXXX: error message, Error message from the application, etc... ",
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
            "id": "problem_start_time",
            "order": 11,
            "controlType": "datetimepicker",
            "displayLabel": "Problem start time",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
