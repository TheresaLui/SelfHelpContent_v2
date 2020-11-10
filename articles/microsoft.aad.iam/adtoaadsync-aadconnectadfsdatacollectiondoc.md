<properties pageTitle="Problem with AAD Connect ADFS" 
	 description="aadconnectadfsdatacollectiondoc" 
	 authors="anupnadigm" 
	 selfHelpType="problemScopingQuestions" 
	 supportTopicIds="32404463" 
	 productPesIds="14785,16578" 
	 cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec" 
	 schemaVersion="1"
    articleId="22605ab0-3d0b-454c-ac3a-e44d1c57086b"
	ownershipId="AzureIdentity_DirectoryObjectManagement"
/> 
# Problem with AAD Connect ADFS 
---
{
    "resourceRequired": false,
    "title": "Problem with AAD Connect ADFS",
    "fileAttachmentHint": null,
    "formElements": [
        {
            "id": "alreadydeployed",
            "visibility": null,
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Have you already deployed AD FS?",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Yes",
                    "value": "ADFSDeployed"
                },
                {
                    "text": "No",
                    "value": "ADFSNotDeployed"
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
            "id": "versionOfADFS",
            "visibility": null,
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What is the version of AD FS farm?",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Server 2016",
                    "value": "version2016"
                },
                {
                    "text": "Server 2012 R2",
                    "value": "version2012R2"
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
            "id": "isMultipleDomain",
            "visibility": null,
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Do you want to federate multiple domains with the AD FS farm?",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Yes",
                    "value": "MultiDomainFederation"
                },
                {
                    "text": "No",
                    "value": "SingleDomainFederation"
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
            "id": "issueHead",
            "visibility": null,
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "What is the task for whch support is needed?",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Deploy AD FS using Azure AD Connect",
                    "value": "DeployADFS"
                },
                {
                    "text": "Add additional AD FS / WAP Server",
                    "value": "AddADFSServer"
                },
                {
                    "text": "Add federation for another domain in Azure AD",
                    "value": "FederateMultipleDomain"
                },
                {
                    "text": "Other",
                    "value": "OtherFederationTask"
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
            "id": "problem_description",
            "visibility": null,
            "order": 5,
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
        },
        {
            "id": "problem_start_time",
            "order": 6,
            "controlType": "datetimepicker",
            "displayLabel": "Problem start time",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---