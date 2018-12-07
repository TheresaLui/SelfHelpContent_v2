<properties
                pageTitle="Cannot Connect to My Virtual Machine"
                description="Cannot Connect to My Virtual Machine"
                authors="summertgu"
                authorAlias="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32615530"
                productPesIds="14749"
                cloudEnvironments="Public"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea1212"
/>
# Connect to a VM
---
{
                "resourceRequired": true,
                "title": "My configuration change impacted connectivity",
                "fileAttachmentHint": "",
                "formElements": [
                {
                "id": "connect_error",
                "order": 1,
                "controlType": "multilinetextbox",
                "displayLabel": "What is the error you received?",
                "required": false,
                "useAsAdditionalDetails": false,
                },{
                    "id": "connect_config",
                    "order": 2,
                    "controlType": "dropdown",
                    "displayLabel": "What was your configuration change prior to the issue starting?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                        {
                            "value": "I pushed an update to my machine",
                            "text": "I pushed an update to my machine"
                        },
                        {
                            "value": "I changed my firewall configuration",
                            "text": "I changed my firewall configuration"
                        },
                        {
                            "value": "I installed a third party app",
                            "text": "I installed a third party app"
                        },{
                            "value": "Other",
                            "text": "Other"
                        }
                    ],
                    "required": false
                },{
                "id": "connect_config_other",
                "order": 3,
                "visibility": "connect_config == Other",
                "controlType": "multilinetextbox",
                "displayLabel": "Please specify your configuration change prior to the issue starting.",
                "required": false,
                "useAsAdditionalDetails": true,
                },{
                    "id": "connect_ifnew",
                    "order": 4,
                    "controlType": "dropdown",
                    "displayLabel": "Is this VM new to Azure?",
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
                    "id": "connect_from",
                    "order": 5,
                    "visibility": "connect_ifnew == Yes",
                    "controlType": "dropdown",
                    "displayLabel": "Where is the VM from?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                        {
                            "value": "On premise",
                            "text": "On premise"
                        },
                        {
                            "value": "From ASM to ARM",
                            "text": "From ASM to ARM"
                        },
                        {
                            "value": "From another cloud provider",
                            "text": "From another cloud provider"
                        }
                    ],
                    "required": false
                },{
                    "id": "connect_ifazuresiterecovery",
                    "order": 6,
                    "visibility": "connect_from == On premise || connect_from == From another cloud provider",
                    "controlType": "dropdown",
                    "displayLabel": "Was this using Azure site recovery?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                        {
                            "value": "I used Azure site recovery",
                            "text": "I used Azure site recovery"
                        },
                        {
                            "value": "I used a third-party migration tool",
                            "text": "I used a third-party migration tool"
                        },
                        {
                            "value": "I uploaded the disk manually",
                            "text": "I uploaded the disk manually"
                        },
                        {
                            "value": "I used Azure Migrate",
                            "text": "I used Azure Migrate"
                        }
                    ],
                    "required": false
                },{
                    "id": "connect_ifbackup",
                    "order": 7,
                    "controlType": "dropdown",
                    "displayLabel": "Was this VM recovered from backup?",
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
                  "order": 8,
                  "controlType": "multilinetextbox",
                  "displayLabel": "Description",
                  "useAsAdditionalDetails": false,
                  "required": true
                  },{
                  "id": "problem_start_time",
                  "order": 9,
                  "controlType": "datetimepicker",
                  "displayLabel": "When did the problem start?",
                  "required": true
                }
                ]
}
---
