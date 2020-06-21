<properties
    pageTitle="AAD Connect synchronization not working"
    description="aadconnectsynchronizationnotworking"
    authors="anupnadigm"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32565591"
    productPesIds="14785,16578"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    schemaVersion="1"
    articleId="1081c592-989c-4a7f-bf06-7438278335e7"
    	ownershipId="AzureIdentity_DirectoryObjectManagement"
/>

# AAD Connect synchronization not working

---
{
    "resourceRequired": false,
    "title": "AAD Connect synchronization not working",
    "fileAttachmentHint": "Upload the ZIP file",
    "formElements": [
        {
            "id": "aadConnector",
            "visibility": "true",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "Azure AD Connect version",
            "content": null,
            "watermarkText": "Please specify the Azure AD Connect version you have. For example, 1.1.425.0.",
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "hints": [],
            "required": false,
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
            "watermarkText": "Please describe the problem you have, including symptoms and errors encountered.",
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
            "id": "isRelatedToWizard",
            "visibility": "true",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Is the issue related to sync configuration change in the wizard?",
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
                    "text": "Don't know",
                    "value": "dontKnow"
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
            "id": "filesToUploadIsRelatedToWizardYes",
            "visibility": "isRelatedToWizard==yes",
            "order": 5,
            "controlType": "infoblock",
            "displayLabel": null,
            "content": "Please share the setup logs. If the Azure AD Connect version you are using is 1.1.443.0 or after, the logs are located under '%programdata%\\AADConnect'. Otherwise, they are located under '%localappdata%\\AADConnect'. Please also provide a copy of the Windows Event logs (Application and System) when the problem occurred. Put all the content to be shared into a single ZIP file and upload the file using 'File upload' on the left.",
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
            "id": "filesToUploadIsRelatedToWizardDontKnow",
            "visibility": "isRelatedToWizard==dontKnow",
            "order": 6,
            "controlType": "infoblock",
            "displayLabel": null,
            "content": "Please share the setup logs. If the Azure AD Connect version you are using is 1.1.443.0 or after, the logs are located under '%programdata%\\AADConnect'. Otherwise, they are located under '%localappdata%\\AADConnect'. Please also provide a copy of the Windows Event logs (Application and System) when the problem occurred. Put all the content to be shared into a single ZIP file and upload the file using 'File upload' on the left.",
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
            "id": "filesToUploadIsRelatedToWizardNo",
            "visibility": "isRelatedToWizard==no",
            "order": 7,
            "controlType": "infoblock",
            "displayLabel": null,
            "content": "Please provide a copy of the Windows Event logs (Application and System) when the problem occurred. Put all the content to be shared into a single ZIP file and upload the file using 'File upload' on the left.",
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
            "order": 8,
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