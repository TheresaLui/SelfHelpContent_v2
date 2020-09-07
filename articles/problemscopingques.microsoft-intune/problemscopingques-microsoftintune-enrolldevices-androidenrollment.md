<properties
	pageTitle="Enroll Devices - Android enrollment"
	description="Enroll Devices - Android enrollment"
	authors="mackie1604"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32599597"
	productPesIds="15584"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="363b77ba-c498-4b5e-84e1-aa417a79c539"
	ownershipId="IntuneCxP_Intune"
/>
# Enroll Devices - Android enrollment
---
{
    "resourceRequired": false,
    "title": "Enroll Devices - Android enrollment",
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
            "id": "Android_problem_determination",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What problem are you having?",
            "watermarkText": "Choose a problem",
            "dropdownOptions": [
                {
                    "value": "Cannot enroll Android device(s)",
                    "text": "Cannot enroll Android device(s)"
                },
                {
                    "value": "Cannot enroll Android for Work device(s)",
                    "text": "Cannot enroll Android for Work device(s)"
                },
                {
                    "value": "Cannot setup Android for Work binding",
                    "text": "Cannot setup Android for Work binding"
                },
                {
                    "value": "Cannot remove Android for Work binding",
                    "text": "Cannot remove Android for Work binding"
                },
                {
                    "value": "Cannot login to Company Portal application to enroll a device",
                    "text": "Cannot login to Company Portal application to enroll a device"
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
            "id": "What device OEM is impacted?",
            "order": 4,
            "controlType": "multiselectdropdown",
            "displayLabel": "Select device types that are impacted",
            "dropdownOptions": [
                {
                    "value": "Samsung non-Knox",
                    "text": "Samsung non-Knox"
                },
                {
                    "value": "Samsung Knox",
                    "text": "Samsung Knox"
                },
                {
                    "value": "Google",
                    "text": "Google"
                },
                {
                    "value": "Sony",
                    "text": "Sony"
                },
                {
                    "value": "LG",
                    "text": "LG"
                },
                {
                    "value": "HTC",
                    "text": "HTC"
                },
                {
                    "value": "Huawei",
                    "text": "Huawei"
                },
                {
                    "value": "Motorola",
                    "text": "Motorola"
                },
                {
                    "value": "Other",
                    "text": "Other"
                }
            ],
            "required": false
        },
        {
            "id": "How are these devices managed?",
            "order": 5,
            "controlType": "multiselectdropdown",
            "displayLabel": "How are these devices managed?",
            "dropdownOptions": [
                {
                    "value": "Bring-your-own-device (BYOD)",
                    "text": "Bring-your-own-device (BYOD)"
                },
                {
                    "value": "Corporate-owned",
                    "text": "Corporate-owned"
                }
            ],
            "required": false
        },
        {
            "id": "How many users are impacted?",
            "order": 6,
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
            "order": 7,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 8,
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
