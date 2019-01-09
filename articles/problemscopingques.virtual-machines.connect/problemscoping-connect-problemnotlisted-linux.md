<properties
                pageTitle="Cannot Connect to My Virtual Machine"
                description="Cannot Connect to My Virtual Machine"
                authors="summertgu"
                authorAlias="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32615531"
                productPesIds="15571,15797,16454,16470"
                cloudEnvironments="Public"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0017"
/>
# Connect to a VM
---
{
                "resourceRequired": true,
                "title": "My problem is not listed above",
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
                    "id": "connect_config",
                    "order": 2,
                    "controlType": "dropdown",
                    "displayLabel": "What was your configuration change prior to the issue started?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                        {
                            "value": "I pushed an update on my machine",
                            "text": "I pushed an update on my machine"
                        },
                        {
                            "value": "I changed my firewall configuration",
                            "text": "I changed my firewall configuration"
                        },
                        {
                            "value": "I installed a third-party app",
                            "text": "I installed a third-party app"
                        },{
                            "value": "Other",
                            "text": "Other"
                        }
                    ],
                    "required": false
                },{
                    "id": "ippublicprivate",
                    "order": 3,
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
                      "id": "connect_request",
                      "order": 8,
                      "controlType": "dropdown",
                      "displayLabel": "What do you need help with?",
                      "watermarkText": "Choose an option",
                      "dropdownOptions": [{
                        "value": "Recover my VM from a boot failure",
                        "text": "Recover my VM from a boot failure"
                        },{
                        "value": "Recreate the Virtual Machine",
                        "text": "Recreate the Virtual Machine"
                        },{
                        "value": "Root cause analysis",
                        "text": "Root cause analysis"
                        }
                        ],
                        "required": false
                    },{
                    "id": "connect_ifinternet",
                    "order": 9,
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
                    "order": 10,
                    "controlType": "multilinetextbox",
                    "displayLabel": "Description",
                    "useAsAdditionalDetails": false,
                    "required": true
                    },{
                    "id": "problem_start_time",
                    "order": 11,
                    "controlType": "datetimepicker",
                    "displayLabel": "When did the problem start?",
                    "required": true
                  }
                  ]
}
---
