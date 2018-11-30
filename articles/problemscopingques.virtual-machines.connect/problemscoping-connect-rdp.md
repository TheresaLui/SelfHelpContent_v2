<properties
                pageTitle="Cannot Connect to My Virtual Machine"
                description="Cannot Connect to My Virtual Machine"
                authors="tiag"
                authorAlias="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32615526"
                productPesIds="14749"
                cloudEnvironments="Public"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea1212"
/>
# Connect to a VM
---
{
                "resourceRequired": true,
                "title": "Failure to connect to the RDP port",
                "fileAttachmentHint": "",
                "formElements": [
                {
                "id": "connect_error",
                "order": 1,
                "controlType": "multilinetextbox",
                "displayLabel": "What is the error you received?",
                "required": false,
                "useAsAdditionalDetails": true,
                "hints": [{
                  "text": "Copy and paste the specific error from the activity log."
                  }]
                },{
                    "id": "ippublicprivate",
                    "order": 2,
                    "controlType": "dropdown",
                    "displayLabel": "Are you using a Public or Private IP?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                        {
                            "value": "Public IP",
                            "text": "Public IP"
                        },
                        {
                            "value": "Private IP",
                            "text": "Private IP"
                        }
                    ],
                    "required": false
                },{
                    "id": "iswindowsnano",
                    "order": 3,
                    "controlType": "dropdown",
                    "displayLabel": "Is this a Windows Nano machine?",
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
                    "id": "isnewvm",
                    "order": 4,
                    "controlType": "dropdown",
                    "displayLabel": "Is this a new VM in azure?",
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
                    "id": "wassetupcorrect",
                    "order": 5,
                    "controlType": "dropdown",
                    "displayLabel": "Was the VM set up correctly to work in cloud environment?",
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
                  "id": "problem_description",
                  "order": 6,
                  "controlType": "multilinetextbox",
                  "displayLabel": "Description",
                  "useAsAdditionalDetails": false,
                  "required": true
                  }
                  ]
}
---
