<properties
    pageTitle="Azure AD Connect synchronization issue with specific attribute"
    description="aadconnectsynchronizationproblemforaspecificattribute"
    authors="anupnadigm"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32565590"
    productPesIds="14785"
    cloudEnvironments="public"
    schemaVersion="1"
    articleId="c3f74466-ee43-4568-9ae0-2258be8d4bb1"
    />

# Azure AD Connect synchronization issue with specific attribute

---
{
    "resourceRequired": false,
    "title": "Azure AD Connect synchronization issue with specific attribute",
    "fileAttachmentHint": "Upload the ZIP file",
    "formElements": [
        {
            "id": "aadConnector",
            "visibility": "true",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "Azure AD Connect version",
            "content": null,
            "watermarkText": "Please specify the Azure AD Connect version you have. For example, 1.1.552.0.",
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "hints": [],
            "required": true,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 1
        },
        {
            "id": "problemDetails",
            "visibility": "true",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the problem?",
            "content": null,
            "watermarkText": "Please describe the problem you have, including symptoms and errors encountered. If you have received notification of synchronization error for this issue, please paste the error details and include the TrackingId (if available).",
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
            "id": "problem_start_time",
            "visibility": null,
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem occur?",
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
            "id": "whatTriggeredTheIssue",
            "visibility": "true",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Is the problem caused by one of the following changes?",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Configuration change made in Azure AD Connect wizard",
                    "value": "configChangeInWizard"
                },
                {
                    "text": "Changes made to synchronization rules",
                    "value": "syncRuleChange"
                },
                {
                    "text": "Don't know / Other",
                    "value": "dontKnowOrOther"
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
            "id": "askForSetupLogs",
            "visibility": "whatTriggeredTheIssue==configChangeInWizard",
            "order": 5,
            "controlType": "infoblock",
            "displayLabel": null,
            "content": "Please share the setup logs. If the Azure AD Connect version is 1.1.443.0 or after, the logs are located under '%programdata%\\\\AADConnect'. Otherwise, they are located under '%localappdata%\\\\AADConnect'. Please share provide the entire folder.",
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
            "id": "askForSyncRules",
            "visibility": "whatTriggeredTheIssue==syncRuleChange",
            "order": 6,
            "controlType": "infoblock",
            "displayLabel": null,
            "content": "Please run cmdlet Get-ADSyncRule and save the output to a text file. Put all the content to be shared into a single ZIP file and upload the file using 'File upload' on the left.",
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