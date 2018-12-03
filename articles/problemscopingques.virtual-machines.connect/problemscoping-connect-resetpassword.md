<properties
                pageTitle="Cannot Connect to My Virtual Machine"
                description="Cannot Connect to My Virtual Machine"
                authors="summertgu"
                authorAlias="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32615529"
                productPesIds="14749"
                cloudEnvironments="Public"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea1212"
/>
# Connect to a VM
---
{
                "resourceRequired": true,
                "title": "I need to reset my password",
                "fileAttachmentHint": "",
                "formElements": [
                {
                    "id": "idlocaldomain",
                    "order": 1,
                    "controlType": "dropdown",
                    "displayLabel": "Is this a local or domain ID?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                        {
                            "value": "Local ID",
                            "text": "Local ID"
                        },
                        {
                            "value": "Domain ID",
                            "text": "Domain ID"
                        }
                    ],
                    "required": false
                },{
                    "id": "idsinglemultiple",
                    "order": 2,
                    "controlType": "dropdown",
                    "displayLabel": "Is this issue impacting a single ID or multiple IDs?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                        {
                            "value": "Single ID",
                            "text": "Single ID"
                        },
                        {
                            "value": "Multiple IDs",
                            "text": "Multiple IDs"
                        }
                    ],
                    "required": false
                },{
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
                },{
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
                },{
                    "id": "resetpasswordmethods",
                    "order": 5,
                    "controlType": "multiselectdropdown",
                    "displayLabel": "Select all the methods you have tried to reset your password.",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                        {
                            "value": "Portal",
                            "text": "Portal"
                        },
                        {
                            "value": "Powershell CLI",
                            "text": "Powershell CLI"
                        },
                        {
                            "value": "Run commands",
                            "text": "Run commands"
                        },
                        {
                            "value": "Custom script extension",
                            "text": "Custom script extension"
                        }
                    ],
                    "required": false
                },{
                  "id": "problem_description",
                  "order": 6,
                  "controlType": "multilinetextbox",
                  "displayLabel": "Description",
                  "useAsAdditionalDetails": true,
                  "required": true
                  },{
                  "id": "problem_start_time",
                  "order": 7,
                  "controlType": "datetimepicker",
                  "displayLabel": "When did the problem start?",
                  "required": true
                }
                ]
}
---
