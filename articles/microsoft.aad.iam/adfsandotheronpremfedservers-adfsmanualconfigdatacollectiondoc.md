<properties pageTitle="Problem with ADFS manual configeration" 
	 description="adfsmanualconfigdatacollectiondoc" 
	 authors="anupnadigm" 
	 selfHelpType="problemScopingQuestions" 
	 supportTopicIds="32570968" 
	 productPesIds="14785" 
	 cloudEnvironments="public, Fairfax" 
	 schemaVersion="1"
	articleId="5dc61c39-e0d2-4fdb-a6c4-80af03fc3b57"
	ownershipId="ASEP_ContentService_Placeholder"
/> 
# Problem with ADFS manual configeration 
---
{
    "resourceRequired": false,
    "title": "Problem with ADFS manual configeration",
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
                    "text": "Server 2012",
                    "value": "version2012"
                },
                {
                    "text": "Server 2008 R2",
                    "value": "version2008R2"
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
            "id": "domainsToFederate",
            "visibility": null,
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Which domains need to be federated?",
            "content": null,
            "watermarkText": "Example: Contoso.com,fabrikam.com",
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