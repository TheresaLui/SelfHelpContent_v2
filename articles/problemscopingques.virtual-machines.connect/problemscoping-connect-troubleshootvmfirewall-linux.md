<properties
                pageTitle="Cannot Connect to My Virtual Machine"
                description="Cannot Connect to My Virtual Machine"
                authors="summertgu"
                authorAlias="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32615534"
                productPesIds="15571,15797,16454,16470"
                cloudEnvironments="Public"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0029"
/>
# Connect to a VM
---
{
                "resourceRequired": true,
                "title": "Troubleshoot my VM firewall",
                "fileAttachmentHint": "",
                "formElements": [
                {
                    "id": "connect_source",
                    "order": 1,
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
                "order": 2,
                "controlType": "multilinetextbox",
                "displayLabel": "What is your source subnet or IP that you are trying to connect from?",
                "required": false,
                "useAsAdditionalDetails": true,
                },{
                    "id": "connect_firewall",
                    "order": 3,
                    "controlType": "dropdown",
                    "displayLabel": "What firewall are you trying to troubleshoot?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                        {
                            "value": "Endian Firewall Community (EFW)",
                            "text": "Endian Firewall Community (EFW)"
                        },
                        {
                            "value": "Third-party firewall",
                            "text": "Third-party firewall"
                        }
                    ],
                    "required": false
                },{
                    "id": "connect_ifinternet",
                    "order": 4,
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
                  "order": 5,
                  "controlType": "multilinetextbox",
                  "displayLabel": "Description",
                  "useAsAdditionalDetails": false,
                  "required": true
                  },{
                  "id": "problem_start_time",
                  "order": 6,
                  "controlType": "datetimepicker",
                  "displayLabel": "When did the problem start?",
                  "required": true
                }
                ]
}
---
