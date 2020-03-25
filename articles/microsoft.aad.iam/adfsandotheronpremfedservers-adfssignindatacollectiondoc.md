<properties pageTitle="Problem with ADFS sign in" 
	 description="adfssignindatacollectiondoc" 
	 authors="anupnadigm" 
	 selfHelpType="problemScopingQuestions" 
	 supportTopicIds="32570971" 
	 productPesIds="14785" 
	 cloudEnvironments="public, Fairfax, Mooncake" 
	 schemaVersion="1"
	articleId="7640a487-6f9f-4a3c-9e53-5c75888cc9f2"
	ownershipId="ASEP_ContentService_Placeholder"
/> 
# Problem with ADFS sign in 
---
{
    "resourceRequired": false,
    "title": "Problem with ADFS sign in",
    "fileAttachmentHint": null,
    "formElements": [
        {
            "id": "userUPN",
            "visibility": null,
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "UPN of one of the affected users?",
            "content": null,
            "watermarkText": "Example: user@contoso.com",
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "hints": [],
            "required": true,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 2
        },
        {
            "id": "isMultipleDomain",
            "visibility": null,
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Are multiple domains federated with the AD FS farm?",
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
            "id": "allUsersImpacted",
            "visibility": null,
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Are all users impacted?",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Yes",
                    "value": "AllUsersImpacted"
                },
                {
                    "text": "No",
                    "value": "SingleOrSelectedUsersImpacted"
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
            "id": "AreaOfImpact",
            "visibility": null,
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Internal / external authentication impacted?",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Internal (within corpnet)",
                    "value": "Internal"
                },
                {
                    "text": "External (via WAP)",
                    "value": "External"
                },
                {
                    "text": "Both Internal and External",
                    "value": "BothInternalExternal"
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
            "id": "whereIsError",
            "visibility": null,
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Where is the error reported during sign-in?",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "At AD FS Sign-in Page",
                    "value": "ErrorOnAdfsPage"
                },
                {
                    "text": "Somewhere in the Application",
                    "value": "ErrorOnApplicationPage"
                },
                {
                    "text": "I don't know",
                    "value": "NotSureErrorLocation"
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
        },
        {
            "id": "problem_start_time",
            "order": 7,
            "controlType": "datetimepicker",
            "displayLabel": "Problem start time",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---