<properties
    pageTitle="Problem with Domains Name domains delete"
    description="domainsdeletedomainname"
    authors="anupnadigm"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32045808"
    productPesIds="14785,16578"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    schemaVersion="1"
    articleId="a8f4e38a-eaf1-43c4-b846-bd216f8631f0"
    	ownershipId="AzureIdentity_DirectoryObjectManagement"
/>

# Problem with Domains Name domains delete

---
{
    "resourceRequired": false,
    "title": "Problem with Domains Name domains delete",
    "fileAttachmentHint": null,
    "formElements": [
        {
            "id": "whichDomain",
            "visibility": null,
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "What is the name of the domain that fails to delete?",
            "content": null,
            "watermarkText": "For example 'contoso.com.'",
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
            "id": "whichTenant",
            "visibility": null,
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the tenantID or intial default domain name of the directory where the custom domain fails to delete?",
            "content": null,
            "watermarkText": "The initial default domain name is something like 'contoso.onmicrosoft.com'.",
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "hints": [],
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 2
        },
        {
            "id": "symptomType",
            "visibility": null,
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the error that you are receiving?",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "hints": [],
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 2
        },
        {
            "id": "MultiTenant",
            "visibility": null,
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Does your organization have another Azure AD or use Office 365?",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "No additional directories",
                    "value": "None"
                },
                {
                    "text": "Yes we have an additional Azure AD or use Office 365",
                    "value": "ContainsMultiple"
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