<properties
	pageTitle="Enroll Devices - Enrollment options"
	description="Enroll Devices - Enrollment options"
	authors="mackie1604"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32599632"
	productPesIds="15584"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="292536da-22ef-4a79-83eb-2d97e13648cf"
	ownershipId="IntuneCxP_Intune"
/>
# Enroll Devices - Enrollment options
---
{
    "resourceRequired": false,
    "title": "Enroll Devices - Enrollment options",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "What service are you having the issue with?",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Select the service impacted",
            "watermarkText": "Choose your service",
            "dropdownOptions": [
                {
                    "value": "Intune Standalone",
                    "text": "Intune Standalone"
                },
                {
                    "value": "Intune Hybrid",
                    "text": "Intune Hybrid"
                },
                {
                    "value": "Intune for Education",
                    "text": "Intune for Education"
                },
                {
                    "value": "Intune Insiders",
                    "text": "Intune Insiders"
                },
                {
                    "value": "Mobile Device Management for Office 365",
                    "text": "Mobile Device Management for Office 365"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "EnrollmentOptions_problem_determination",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What problem are you having?",
            "watermarkText": "Choose a problem",
            "dropdownOptions": [
                {
                    "value": "Cannot configure/deploy Terms and Conditions",
                    "text": "Cannot configure/deploy Terms and Conditions"
                },
                {
                    "value": "Cannot setup enrollment restrictions",
                    "text": "Cannot setup enrollment restrictions"
                },
                {
                    "value": "Cannot setup Multi-Factor Authentication for enrollment",
                    "text": "Cannot setup Multi-Factor Authentication for enrollment"
                },
                {
                    "value": "Cannot setup Device Enrollment Manager(s)",
                    "text": "Cannot setup Device Enrollment Manager(s)"
                },
                {
                    "value": "Cannot setup Device Categories",
                    "text": "Cannot setup Device Categories"
                },
                {
                    "value": "Cannot setup Corporate Device Identifiers",
                    "text": "Cannot setup Corporate Device Identifiers"
                },
                {
                    "value": "Other",
                    "text": "Other"
                }
            ],
            "required": true
        },
        {
            "id": "problem_who_is_impacted",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Who is impacted?",
            "watermarkText": "Enter UPN, e-mail addresses, serial or IMEI numbers here, if multiple separate by semi-colon",
            "useAsAdditionalDetails": false,
            "required": true,
            "hints": [
                {
                    "text": "For user based enrollment provide UPN or e-mail addresses.  For userless enrollment provide serial or IMEI numbers"
                }
            ]
        },
        {
            "id": "What platforms are impacted?",
            "order": 4,
            "controlType": "multiselectdropdown",
            "displayLabel": "What platforms are impacted?",
            "dropdownOptions": [
                {
                    "value": "Apple",
                    "text": "Apple"
                },
                {
                    "value": "Android",
                    "text": "Android"
                },
                {
                    "value": "Windows",
                    "text": "Windows"
                },
                {
                    "value": "Other",
                    "text": "Other"
                }
            ],
            "required": false
        },
        {
            "id": "How many users are impacted?",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Select how many users are impacted",
            "watermarkText": "Users impacted",
            "dropdownOptions": [
                {
                    "value": "Single user",
                    "text": "Single user"
                },
                {
                    "value": "A few users",
                    "text": "A few users"
                },
                {
                    "value": "Most of my users",
                    "text": "Most of my users"
                },
                {
                    "value": "All my users",
                    "text": "All my users"
                }
            ],
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 6,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide these details:",
            "watermarkText": "Enter details here",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Issue description that includes device names, error message(s) and scenario(s) that are failing."
                },
                {
                    "text": "Using file upload on the left, attach a screenshot of the error message(s) or any logs/documentation gathered."
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---
