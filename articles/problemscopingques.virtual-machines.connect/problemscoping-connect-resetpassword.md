<properties
                pageTitle="Cannot Connect to My Virtual Machine"
                description="Cannot Connect to My Virtual Machine"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32615529"
                productPesIds="14749"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0021"
	ownershipId="Compute_VirtualMachines_Content"
/>
# Connect to a VM
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "I need to reset my password",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "idlocaldomain",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Is this for a local user account or a domain user account",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Local user account",
                    "text": "Local user account"
                },
                {
                    "value": "Domain user account",
                    "text": "Domain user account"
                }
            ],
            "required": false
        },
        {
            "id": "useraccountsinglemultiple",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Is this issue impacting a single user account or multiple user accounts?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "A single user account",
                    "text": "A single user account"
                },
                {
                    "value": "Multiple user accounts",
                    "text": "Multiple user accounts"
                }
            ],
            "required": false
        },
        {
            "id": "isdomaincontroller",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Is this machine a domain controller?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "I do not know",
                    "text": "I do not know"
                }
            ],
            "required": false
        },
        {
            "id": "isadmin",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Is this the built-in administrator account?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "I do not know",
                    "text": "I do not know"
                }
            ],
            "required": false
        },
        {
            "id": "name_useraccount",
            "order": 5,
            "visibility": "isadmin == No || isadmin == I do not know",
            "controlType": "textbox",
            "displayLabel": "What is the name of the user account trying to login?",
            "required": false
        },
        {
            "id": "resetpasswordmethods",
            "order": 6,
            "controlType": "multiselectdropdown",
            "displayLabel": "Select all the methods you have tried to reset your password.",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Portal",
                    "text": "Portal"
                },
                {
                    "value": "Powershell or CLI",
                    "text": "Powershell or CLI"
                },
                {
                    "value": "Run Commands or Custom script Extension",
                    "text": "Run Commands or Custom script Extension"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 8,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
