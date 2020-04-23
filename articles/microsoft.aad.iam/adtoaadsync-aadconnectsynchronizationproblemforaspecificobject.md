<properties pageTitle="AAD Connect synchronization problem for a specific object" 
	 description="aadconnectsynchronizationproblemforaspecificobject" 
	 authors="anupnadigm" 
	 selfHelpType="problemScopingQuestions" 
	 supportTopicIds="32570979,32570976,32586796" 
	 productPesIds="14785,16578" 
	 cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec" 
	 schemaVersion="1"
    articleId="cfb77bcc-9d23-4a17-8235-0bdbeede9949"
	ownershipId="AzureIdentity_DirectoryObjectManagement"
/> 
# AAD Connect synchronization problem for a specific object 
---
{
    "resourceRequired": false,
    "title": "AAD Connect synchronization problem for a specific object",
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
            "id": "objectType",
            "visibility": "true",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Please select the type of directory object you have problem with",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "User",
                    "value": "user"
                },
                {
                    "text": "Group",
                    "value": "group"
                },
                {
                    "text": "Contact",
                    "value": "contact"
                },
                {
                    "text": "Computer/Device",
                    "value": "device"
                },
                {
                    "text": "Mail-Enabled Public Folder",
                    "value": "publicFolder"
                },
                {
                    "text": "Other",
                    "value": "otherObjectType"
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
            "id": "aadObjectExist",
            "visibility": "true",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Is there a corresponding Azure AD object created for this on-premises AD object?",
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
            "id": "aadObjectId",
            "visibility": "aadObjectExist==yes",
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