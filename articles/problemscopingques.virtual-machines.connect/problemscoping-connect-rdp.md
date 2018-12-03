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
                    "id": "connect_ifnew",
                    "order": 3,
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
                    "order": 4,
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
                    "order": 5,
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
                    "id": "machinetype",
                    "order": 6,
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
                            "value": "Other",
                            "text": "Other"
                        }
                    ],
                    "required": false
                },{
                "id": "machinetype_other",
                "order": 7,
                "visibility": "machinetype == Other",
                "controlType": "textbox",
                "displayLabel": "Please specify the type of machine you are trying to RDP into.",
                "useAsAdditionalDetails": false,
                "required": false
                },{
                    "id": "iscitrixrds",
                    "order": 8,
                    "controlType": "dropdown",
                    "displayLabel": "Is this machine a Citrix or RDS VM?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                        {
                            "value": "Citrix VM",
                            "text": "Citrix VM"
                        },
                        {
                            "value": "RDS VM",
                            "text": "RDS VM"
                        },
                        {
                            "value": "I do not know",
                            "text": "I do not know"
                        }
                    ],
                    "required": false
                },{
                  "id": "problem_description",
                  "order": 9,
                  "controlType": "multilinetextbox",
                  "displayLabel": "Description",
                  "useAsAdditionalDetails": false,
                  "required": true
                  },{
                  "id": "problem_start_time",
                  "order": 10,
                  "controlType": "datetimepicker",
                  "displayLabel": "When did the problem start?",
                  "required": true
                }
                ]
}
---
