<properties
                pageTitle="Cannot Connect to My Virtual Machine"
                description="Cannot Connect to My Virtual Machine"
                authors="summertgu"
                authorAlias="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32615527"
                productPesIds="14749"
                cloudEnvironments="Public"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0018"
/>
# Connect to a VM
---
{
                "resourceRequired": true,
                "title": "I have an issue with my public IP",
                "fileAttachmentHint": "",
                "formElements": [
                {
                "id": "connect_error",
                "order": 1,
                "controlType": "multilinetextbox",
                "displayLabel": "What is the error you received?",
                "required": false,
                "useAsAdditionalDetails": true
                },{
                    "id": "connect_ifnew",
                    "order": 2,
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
                    "order": 3,
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
                    "order": 4,
                    "visibility": "connect_from == On premise || connect_from == From another cloud provider",
                    "controlType": "dropdown",
                    "displayLabel": "Was this using Azure Site Recovery?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                        {
                            "value": "I used Azure Site Recovery",
                            "text": "I used Azure Site Recovery"
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
                    "id": "machinetype",
                    "order": 5,
                    "controlType": "dropdown",
                    "displayLabel": "From which type of machine are you trying to RDP into?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                        {
                            "value": "Windows 7/Windows server 2008r2",
                            "text": "Windows 7/Windows server 2008r2"
                        },
                        {
                            "value": "Windows 8/Windows server 2012",
                            "text": "Windows 8/Windows server 2012"
                        },
                        {
                            "value": "Windows 8.1/Windows server 2012r2",
                            "text": "Windows 8.1/Windows server 2012r2"
                        },
                        {
                            "value": "Windows 10/Windows server 2016",
                            "text": "Windows 10/Windows server 2016"
                        },
                        {
                            "value": "Android or iOS",
                            "text": "Android or iOS"
                        },
                        {
                            "value": "Citrix or RDS",
                            "text": "Citrix or RDS"
                        }
                    ],
                    "required": false
                },{
                    "id": "connect_ifinternet",
                    "order": 6,
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
                  "order": 7,
                  "controlType": "multilinetextbox",
                  "displayLabel": "Description",
                  "useAsAdditionalDetails": false,
                  "required": true
                  },{
                  "id": "problem_start_time",
                  "order": 8,
                  "controlType": "datetimepicker",
                  "displayLabel": "When did the problem start?",
                  "required": true
                }
                ]
}
---
