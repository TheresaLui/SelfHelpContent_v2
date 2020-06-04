<properties pageTitle="Azure AD Connect password synchronization issue" 
	 description="aadconnectpasswordsynchronizationissues" 
	 authors="anupnadigm" 
	 selfHelpType="problemScopingQuestions" 
	 supportTopicIds="32142240" 
	 productPesIds="14785,16578" 
	 cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec" 
	 schemaVersion="1"
    articleId="7270fcb1-252a-4ff9-ad8c-e4a58a978d55"
	ownershipId="AzureIdentity_DirectoryObjectManagement"
/> 
# Azure AD Connect password synchronization issue 
---
{
    "resourceRequired": false,
    "title": "Azure AD Connect password synchronization issue",
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
            "watermarkText": "Please describe the problem you have, including symptoms and errors encountered. If you have received notification of synchronization error for this issue, please paste the error details and include the TrackingId (if available).",
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
            "id": "problemScope",
            "visibility": "true",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Please select the scope of problem you have",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Issue is specific to a particular user",
                    "value": "specificObject"
                },
                {
                    "text": "Password Synchronization process is not working and is affecting many or all users",
                    "value": "global"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
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
            "id": "filesToUploadSpecificObjectIssue",
            "visibility": "problemScope==specificObject",
            "order": 5,
            "controlType": "infoblock",
            "displayLabel": null,
            "content": "Please provide a copy of the Windows Event logs (Application and System) around the time when the problem occurred. Put all the content to be shared into a single ZIP file and upload it using 'File upload' option on the left.",
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
            "id": "aadObjectId",
            "visibility": "problemScope==specificObject",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Azure AD Object Identifier",
            "content": null,
            "watermarkText": "Please specify the ObjectID or userPrincipalName of the Azure AD object.",
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
            "id": "filesToUploadGlobalIssue",
            "visibility": "problemScope==global",
            "order": 7,
            "controlType": "infoblock",
            "displayLabel": null,
            "content": "Please provide a copy of the Windows Event logs (Application and System) around the time when the problem occurred. Please also share your Azure AD Connect server configuration by running Get-ADSyncGlobalSettingsParameter cmdlet on the server and saving the output to a text file. Put all the content to be shared into a single ZIP file and upload it using 'File upload' option on the left.",
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