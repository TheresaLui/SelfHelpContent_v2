<properties pageTitle="Azure AD Connect issue with database" 
	 description="aadconnectsqlrelatedinstallationandsyncissue" 
	 authors="anupnadigm" 
	 selfHelpType="problemScopingQuestions" 
	 supportTopicIds="32565592" 
	 productPesIds="14785,16578" 
	 cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec" 
	 schemaVersion="1"
    articleId="5ce95b3b-058d-4b0f-b1f6-539bc069294a"
	ownershipId="AzureIdentity_DirectoryObjectManagement"
/> 
# Azure AD Connect issue with database 
---
{
    "resourceRequired": false,
    "title": "Azure AD Connect issue with database",
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
            "id": "dBConfig",
            "visibility": "true",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What database is the Azure AD Connect server currently using?",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "LocalDB",
                    "value": "localDB"
                },
                {
                    "text": "Full SQL installed on the same server as Azure AD Connect",
                    "value": "fullSQLLocal"
                },
                {
                    "text": "Full SQL installed on a different server than Azure AD Connect",
                    "value": "fullSQLRemote"
                },
                {
                    "text": "Other",
                    "value": "otherDBConfig"
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
            "id": "problemDetails",
            "visibility": "true",
            "order": 3,
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
            "order": 4,
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
            "id": "filesToUpload",
            "visibility": "true",
            "order": 5,
            "controlType": "infoblock",
            "displayLabel": null,
            "content": "Please provide a copy of the Windows Event logs (Application and System) during when the problem occurred. Put all the content to be shared into a single ZIP file and upload the file using 'File upload' on the left.",
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
            "order": 6,
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