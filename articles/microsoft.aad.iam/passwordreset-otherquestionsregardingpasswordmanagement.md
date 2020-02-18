<properties
    pageTitle="Other problems with password reset"
    description="otherquestionsregardingpasswordmanagement"
    authors="anupnadigm"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32565599"
    productPesIds="14785,16578,16575"
    cloudEnvironments="public"
    schemaVersion="1"
    articleId="4077bf1c-7ac9-4eb2-8a44-152c9f92d9c5"
    />

# Other problems with password reset

---
{
    "resourceRequired": false,
    "title": "Other problems with password reset",
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
            "id": "scope",
            "visibility": null,
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Which aspect of the feature are you having difficulty with?",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Password reset reports/audit logs",
                    "value": "audit"
                },
                {
                    "text": "Password reset registration",
                    "value": "register"
                },
                {
                    "text": "Other, don't know or not applicable",
                    "value": "na"
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
            "id": "hasSupportCode",
            "visibility": "true",
            "order": 4,
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
            "order": 5,
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
            "order": 6,
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