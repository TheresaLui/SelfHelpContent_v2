<properties
    pageTitle="Problem with passowrd write back"
    description="passwordwriteback"
    authors="anupnadigm"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32565598"
    productPesIds="14785,16578,16575"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    schemaVersion="1"
    articleId="7d573624-e0cc-47f2-8da7-3e175d927dc5"
    	ownershipId="AzureIdentity_DirectoryObjectManagement"
/>

# Problem with passowrd write back

---
{
    "resourceRequired": false,
    "title": "Problem with passowrd write back",
    "fileAttachmentHint": null,
    "formElements": [
        {
            "id": "error",
            "visibility": "true",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "What is the exact error message you see?",
            "content": null,
            "watermarkText": "Please enter what error you see verbatim",
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
            "id": "upn",
            "visibility": "true",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Please list all of the affected UPN (User Principal Name)",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "hints": [],
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 5
        },
        {
            "id": "hasSupportCode",
            "visibility": "true",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Do you have a support code/correlation ID for an error related to this problem?",
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
                    "text": "Other, don't know or not applicable",
                    "value": "other"
                }
            ],
            "dynamicDropdownOptions": null,
            "hints": [],
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "ifCorrelationID",
            "visibility": "hasSupportCode==yes",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Support Code/Correlation ID",
            "content": null,
            "watermarkText": "Enter the support code found at the bottom-right of the password reset page",
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
            "id": "getCorrelationID",
            "visibility": "hasSupportCode!=yes",
            "order": 5,
            "controlType": "infoblock",
            "displayLabel": null,
            "content": "<a href='https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#contact-microsoft-support'>Microsoft can provide a solution to your problem faster if you can provide the support code found at the bottom-right of the password reset page</a>",
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
            "visibility": "true",
            "order": 6,
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