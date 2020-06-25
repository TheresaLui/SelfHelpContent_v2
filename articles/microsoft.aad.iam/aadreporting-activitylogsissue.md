<properties pageTitle="Problem with Activity logs in Azure AD" 
	 description="activitylogsissue" 
	 authors="anupnadigm" 
	 selfHelpType="problemScopingQuestions" 
	 supportTopicIds="32574686,32574683" 
	 productPesIds="14785,16577" 
	 cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec" 
	 schemaVersion="1"
    articleId="1387d93d-ec85-45fa-9463-efaf4c3a8855"
	ownershipId="AzureIdentity_ComplianceAndReporting"
/> 
# Problem with Activity logs in Azure AD 
---
{
    "resourceRequired": true,
    "title": "Problem with Activity logs in Azure AD",
    "fileAttachmentHint": null,
    "formElements": [
        {
            "id": "Whichenv",
            "visibility": null,
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Which environment are you using?",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Azure Portal",
                    "value": "AP"
                },
                {
                    "text": "O365 Admin Portal",
                    "value": "O365"
                },
                {
                    "text": "Microsoft Graph APIs",
                    "value": "API"
                },
                {
                    "text": "Azure AD Power BI Content Pack",
                    "value": "PBI"
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
            "id": "dataretention",
            "visibility": "whichenv==AP",
            "order": 2,
            "controlType": "infoblock",
            "displayLabel": null,
            "content": "You are currently using Azure portal",
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
            "id": "tenantSubs",
            "visibility": null,
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Does your tenant have Azure AD Premium 1 or 2 license?",
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
            "id": "whichactivity",
            "visibility": null,
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Which activity data are you having problem with?",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Sign-ins",
                    "value": "signins"
                },
                {
                    "text": "Audit",
                    "value": "audit"
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
            "id": "Whichissue",
            "visibility": null,
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "What issue is this related to?",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "I can't find all the activity logs in my downloaded/exported file",
                    "value": "missingdatadownload"
                },
                {
                    "text": "I can't find actions that have been recently performed in Azure AD through activity logs",
                    "value": "latencydata"
                },
                {
                    "text": "I can't find activity logs beyond 30 days (Premium tenants) or 7 days (free/basic tenants)",
                    "value": "dataretentionFree"
                },
                {
                    "text": "Other issues",
                    "value": "other"
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
            "id": "faqInfo",
            "visibility": "Whichissue!=other",
            "order": 6,
            "controlType": "infoblock",
            "displayLabel": null,
            "content": "<a href='https://docs.microsoft.com/azure/active-directory/active-directory-reporting-faq'>Check out the frequently asked questions about Activity logs here.</a>",
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
            "id": "problem_start_time",
            "visibility": null,
            "order": 7,
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
            "id": "symptoms",
            "visibility": null,
            "order": 8,
            "controlType": "multilinetextbox",
            "displayLabel": "What are the symptoms of the problem?",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "hints": [],
            "required": true,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 4
        },
        {
            "id": "problem_description",
            "visibility": null,
            "order": 9,
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