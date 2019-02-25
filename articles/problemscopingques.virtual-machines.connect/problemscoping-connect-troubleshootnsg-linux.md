<properties
                pageTitle="Cannot Connect to My Virtual Machine"
                description="Cannot Connect to My Virtual Machine"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32615533"
                productPesIds="15571,15797,16454,16470"
                cloudEnvironments="Public"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0027"
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
                "useAsAdditionalDetails": true
                },{
                    "id": "ippublicprivate",
                    "order": 2,
                    "controlType": "dropdown",
                    "displayLabel": "Do you have issues connecting via Public or Private IP?",
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
                    "id": "ippublic",
                    "order": 3,
                    "visibility": "ippublicprivate == Public IP",
                    "controlType": "dropdown",
                    "displayLabel": "Are you able to connect to the Private IP?",
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
                    "id": "ipprivate",
                    "order": 4,
                    "visibility": "ippublicprivate == Private IP",
                    "controlType": "dropdown",
                    "displayLabel": "Are you able to connect to the Public IP?",
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
                            "value": "I don't have a Public IP",
                            "text": "I don't have a Public IP"
                        }
                    ],
                    "required": false
                },{
                    "id": "connect_subnet",
                    "order": 5,
                    "visibility": "ippublic == No || ipprivate == No || ipprivate == I don't have a Public IP",
                    "controlType": "dropdown",
                    "displayLabel": "Is the problem isolated when you are connecting from a specific subnet?",
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
                    "id": "connect_ifnew",
                    "order": 6,
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
                    "order": 7,
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
                    "id": "connect_howmigrated",
                    "order": 8,
                    "visibility": "connect_from == On premise || connect_from == From another cloud provider",
                    "controlType": "dropdown",
                    "displayLabel": "How was this machine migrated?",
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
                    "id": "connect_wasoncloud",
                    "order": 9,
                    "visibility": "connect_from == On premise",
                    "controlType": "dropdown",
                    "displayLabel": "Was the machine prepared to work on a cloud environment prior the migration?",
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
                    "id": "connect_ifinternet",
                    "order": 10,
                    "controlType": "dropdown",
                    "displayLabel": "Do you have connectivity issues from/to this VM?",
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
                    "id": "connect_internetissue",
                    "order": 11,
                    "visibility": "connect_ifinternet == Yes",
                    "controlType": "dropdown",
                    "displayLabel": "What is the problem you are having?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                        {
                            "value": "Cannot connect to the SSH port",
                            "text": "Cannot connect to the SSH port"
                        },
                        {
                            "value": "Cannot connect to the Powershell port",
                            "text": "Cannot connect to the Powershell port"
                        },
                        {
                            "value": "Cannot connect to my SQL instance",
                            "text": "Cannot connect to my SQL instance"
                        },
                        {
                            "value": "Cannot connect to another port",
                            "text": "Cannot connect to another port"
                        },
                        {
                            "value": "My VM doesn't have access to Internet",
                            "text": "My VM doesn't have access to Internet"
                        }
                    ],
                    "required": false
                },{
                  "id": "problem_description",
                  "order": 12,
                  "controlType": "multilinetextbox",
                  "displayLabel": "Description",
                  "useAsAdditionalDetails": false,
                  "required": true
                  },{
                  "id": "problem_start_time",
                  "order": 13,
                  "controlType": "datetimepicker",
                  "displayLabel": "When did the problem start?",
                  "required": true
                }
                ]
}
---
