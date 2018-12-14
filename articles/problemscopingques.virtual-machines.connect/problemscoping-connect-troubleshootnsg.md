<properties
                pageTitle="Cannot Connect to My Virtual Machine"
                description="Cannot Connect to My Virtual Machine"
                authors="summertgu"
                authorAlias="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32615533"
                productPesIds="14749"
                cloudEnvironments="Public"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea1212"
/>
# Connect to a VM
---
{
                "resourceRequired": true,
                "title": "Troubleshoot my network security group (NSG)",
                "fileAttachmentHint": "",
                "formElements": [
                {
                "id": "connect_error",
                "order": 1,
                "controlType": "multilinetextbox",
                "displayLabel": "What is the error you received?",
                "required": false,
                "useAsAdditionalDetails": true,
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
                    "id": "connect_source",
                    "order": 3,
                    "controlType": "dropdown",
                    "displayLabel": "From where are you trying to connect?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                        {
                            "value": "On premise",
                            "text": "On premise"
                        },
                        {
                            "value": "Another machine in Azure",
                            "text": "Another machine in Azure"
                        },
                        {
                            "value": "Another cloud provider",
                            "text": "Another cloud provider"
                        }
                    ],
                    "required": false
                },{
                "id": "connect_sourcesubnetip",
                "order": 4,
                "controlType": "multilinetextbox",
                "displayLabel": "What is your source subnet or IP that you are trying to connect from?",
                "required": false,
                "useAsAdditionalDetails": false,
                },{
                    "id": "connect_ifinternet",
                    "order": 5,
                    "controlType": "dropdown",
                    "displayLabel": "Do you have Internet connectivity issues from this VM?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                        {
                            "value": "Yes",
                            "text": "Yes"
                        },
                        {
                            "value": "No",
                            "text": "No"
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
