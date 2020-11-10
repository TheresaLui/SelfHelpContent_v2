<properties
	pageTitle="Intune Enrollment Android"
	description="Intune Enrollment Android"
	authors="mackie1604"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32530432"
	productPesIds="15584"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="d295eadf-ca63-4106-8564-5f643eced134"
	ownershipId="IntuneCxP_Intune"
/>
# Intune Enrollment Android
---
{
    "resourceRequired": false,
    "title": "Intune Enrollment Android",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "learn_more_text",
            "order": 1,
            "controlType": "infoblock",
            "content": "<b>Review the resources listed as they may help you solve your issue without needing to open a support case</b>  <ul><li>Diagnose end-user issues with the <a href='https://aka.ms/intunetroubleshooting1'>Troubleshooting Portal</a></li>  <li>Review enrollment documentation for <a href='https://docs.microsoft.com/intune/android-enroll'>Android</a></li>  <li>Check out <a href='https://portal.office.com/AdminPortal/Home#/MessageCenter'>Service health</a> and <a href='https://portal.office.com/AdminPortal/Home#/MessageCenter'>Message Center</a> posts to see current status of the service</li>  <li>Review Intune TechNet <a href='https://aka.ms/intuneforums'>forums</a> to find answers and solutions to common issues</li></ul>"
        },
        {
            "id": "What service are you having the issue with?",
            "order": 2,
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
            "order": 3,
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
            "order": 4,
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
            "order": 5,
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
            "order": 6,
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
            "order": 7,
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
            "order": 8,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 11,
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
