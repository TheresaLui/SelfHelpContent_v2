<properties
	pageTitle="Enroll Devices - iOS Enrollment"
	description="Enroll Devices - iOS Enrollment"
	authors="mackie1604"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32599644"
	productPesIds="15584"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="6a980956-8f4d-45bf-811a-03a30719b024"
	ownershipId="IntuneCxP_Intune"
/>
# Enroll Devices - iOS Enrollment
---
{
    "resourceRequired": false,
    "title": "Enroll Devices - iOS Enrollment",
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
            "id": "iOSMAC_problem_determination",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What problem are you having?",
            "watermarkText": "Choose a problem",
            "dropdownOptions": [
                {
                    "value": "Cannot enroll Apple device(s)",
                    "text": "Cannot enroll Apple device(s)"
                },
                {
                    "value": "Cannot setup Apple MDM Push Certificate",
                    "text": "Cannot setup Apple MDM Push Certificate"
                },
                {
                    "value": "Cannot configure Apple Configurator Profile",
                    "text": "Cannot configure Apple Configurator Profile"
                },
                {
                    "value": "Cannot login to Company Portal application to enroll a device",
                    "text": "Cannot login to Company Portal application to enroll a device"
                },
                {
                    "value": "Cannot setup Apple Device Enrollment (DEP) Program or Apple School Manager (ASM) token",
                    "text": "Cannot setup Apple Device Enrollment (DEP) Program or Apple School Manager (ASM) token"
                },
                {
                    "value": "Cannot configure Enrollment Program Profile",
                    "text": "Cannot configure Enrollment Program Profile"
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
            "id": "What devices types are impacted?",
            "order": 4,
            "controlType": "multiselectdropdown",
            "displayLabel": "Select device types that are impacted",
            "dropdownOptions": [
                {
                    "value": "iPad",
                    "text": "iPad"
                },
                {
                    "value": "iPhone",
                    "text": "iPhone"
                },
                {
                    "value": "iPod",
                    "text": "iPod"
                },
                {
                    "value": "Mac",
                    "text": "Mac"
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
                },
                {
                    "value": "Device Enrollment Program (DEP)",
                    "text": "Device Enrollment Program (DEP)"
                },
                {
                    "value": "Apple School Manager (ASM)",
                    "text": "Apple School Manager (ASM)"
                },
                {
                    "value": "Apple Configurator",
                    "text": "Apple Configurator"
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
