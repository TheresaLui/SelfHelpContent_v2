<properties
	pageTitle="Intune Enrollment Windows"
	description="Intune Enrollment Windows"
	authors="mackie1604"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32530438"
	productPesIds="15584"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="d73b7cb8-224c-4a21-8390-2bcc03b11948"
	ownershipId="IntuneCxP_Intune"
/>
# Intune Enrollment Windows
---
{
    "resourceRequired": false,
    "title": "Intune Enrollment Windows",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "learn_more_text",
            "order": 1,
            "controlType": "infoblock",
            "content": "Review the resources listed as they may help you solve your issue without needing to open a support case. Diagnose end-user issues with the <a href='https://aka.ms/intunetroubleshooting1'>Troubleshooting Portal</a>. Review enrollment documentation for <a href='https://docs.microsoft.com/intune/windows-enroll'>Windows</a>. Check out <a href='https://portal.office.com/AdminPortal/Home#/MessageCenter'>Service health</a> and <a href='https://portal.office.com/AdminPortal/Home#/MessageCenter'>Message Center</a> posts to see current status of the service. Review Intune TechNet <a href='https://aka.ms/intuneforums'>forums</a> to find answers and solutions to common issues."
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
            "id": "Windows_problem_determination",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "What problem are you having?",
            "watermarkText": "Choose a problem",
            "dropdownOptions": [
                {
                    "value": "Cannot enroll Windows device(s)",
                    "text": "Cannot enroll Windows device(s)"
                },
                {
                    "value": "Cannot setup Windows 10 automatic enrollment",
                    "text": "Cannot setup Windows 10 automatic enrollment"
                },
                {
                    "value": "Cannot setup bulk enrollment for Windows 10",
                    "text": "Cannot setup bulk enrollment for Windows 10"
                },
                {
                    "value": "Cannot login to Company Portal application to enroll a device",
                    "text": "Cannot login to Company Portal application to enroll a device"
                },
                {
                    "value": "Cannot setup Windows AutoPilot Deployment Program",
                    "text": "Cannot setup Windows AutoPilot Deployment Program"
                },
                {
                    "value": "Cannot setup Windows Hello for Business",
                    "text": "Cannot setup Windows Hello for Business"
                },
                {
                    "value": "Cannot validate CNAME",
                    "text": "Cannot validate CNAME"
                },
                {
                    "value": "Cannot configure Enrollment Status Screen",
                    "text": "Cannot configure Enrollment Status Screen"
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
            "id": "What Operating System(s) are impacted?",
            "order": 5,
            "controlType": "multiselectdropdown",
            "displayLabel": "What Operating System(s) are impacted?",
            "dropdownOptions": [
                {
                    "value": "Windows 10 1511 or earlier",
                    "text": "Windows 10 1511 or earlier"
                },
                {
                    "value": "Windows 10 1607",
                    "text": "Windows 10 1607"
                },
                {
                    "value": "Windows 10 1703",
                    "text": "Windows 10 1703"
                },
                {
                    "value": "Windows 10 1709 or greater",
                    "text": "Windows 10 1709 or greater"
                },
                {
                    "value": "Windows 8.1",
                    "text": "Windows 8.1"
                },
                {
                    "value": "Windows 10 Mobile",
                    "text": "Windows 10 Mobile"
                },
                {
                    "value": "Windows 8 Mobile",
                    "text": "Windows 8 Mobile"
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
                },
                {
                    "value": "Intune for Education",
                    "text": "Intune for Education"
                },
                {
                    "value": "Co-management",
                    "text": "Co-management"
                },
                {
                    "value": "AutoPilot",
                    "text": "AutoPilot"
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
            "order": 9,
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
