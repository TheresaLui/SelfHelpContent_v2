<properties
                pageTitle="Configuration and Setup"
                description="Configuration and Setup"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32539972,32539973"
                productPesIds="10680"
                cloudEnvironments="Public"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0106"
/>
# Config and Setup
---
{
                "resourceRequired": true,
                "title": "Deploy VM Scale Sets",
                "fileAttachmentHint": "",
                "formElements": [
                {
                  "id": "deploy_error",
                  "order": 1,
                  "controlType": "multilinetextbox",
                  "displayLabel": "What is the error you are getting?",
                  "useAsAdditionalDetails": false,
                  "required": true
                  },{
                    "id": "correlation_id",
                    "order": 2,
                    "controlType": "textbox",
                    "displayLabel": "Correlation ID",
                    "required": true
                  },{
                    "id": "deployment_operation",
                    "order": 3,
                    "controlType": "dropdown",
                    "displayLabel": "What operation are you trying to do?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [{
                      "value": "Create",
                      "text": "Create"
                      },{
                      "value": "Start",
                      "text": "Start"
                      },{
                      "value": "Resize",
                      "text": "Resize"
                      },{
                      "value": "Redeploy",
                      "text": "Redeploy"
                      },{
                      "value": "Scale in or out",
                      "text": "Scale in or out"
                      },{
                      "value": "Scale up or down",
                      "text": "Scale up or down"
                      },{
                      "value": "I do not know",
                      "text": "I do not know"
                      }
                      ],
                      "required": false
                  },{
                    "id": "deployment_scenario",
                    "order": 4,
                    "controlType": "dropdown",
                    "displayLabel": "Which of the following describes your scenario?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [{
                      "value": "Add VMs to an existing availability set VMs",
                      "text": "Add VMs to an existing availability set VMs"
                      },{
                        "value": "Allocation failures for older VM sizes",
                        "text": "Allocation failures for older VM sizes"
                      },{
                        "value": "VMSS Scaling",
                        "text": "VMSS Scaling"
                      }
                      ],
                        "required": false
                  },{
                        "id": "deployment_manageddisks",
                        "order": 5,
                        "controlType": "dropdown",
                        "displayLabel": "Are you deploying with managed disks?",
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
                        "id": "deployment_method",
                        "order": 6,
                        "controlType": "dropdown",
                        "displayLabel": "How are you deploying your VMSS?",
                        "watermarkText": "Choose an option",
                        "dropdownOptions": [
                            {
                                "value": "ARM",
                                "text": "ARM"
                            },
                            {
                                "value": "Powershell",
                                "text": "Powershell"
                            },
                            {
                                "value": "CLI",
                                "text": "CLI"
                            },
                            {
                                "value": "Other",
                                "text": "Other"
                            }
                        ],
                        "required": false
                    },{
                          "id": "deployment_from",
                          "order": 7,
                          "controlType": "dropdown",
                          "displayLabel": "What are you trying to create your VMSS from?",
                          "watermarkText": "Choose an option",
                          "dropdownOptions": [{
                            "value": "VHD file",
                            "text": "VHD file"
                            },{
                              "value": "Snapshot",
                              "text": "Snapshot"
                            },{
                              "value": "Captured image",
                              "text": "Captured image"
                              },{
                              "value": "Backup",
                              "text": "Backup"
                            }
                            ],
                              "required": false
                            },{
                    "id": "problem_snapshot_date",
                    "order": 8,
                    "visibility": "deployment_from == Snapshot",
                    "controlType": "datetimepicker",
                    "displayLabel": "What was the time of the attempted snapshot?",
                    "required": true
                    },{
                    "id": "problem_caputre_date",
                    "order": 8,
                    "visibility": "deployment_from == Captured image",
                    "controlType": "datetimepicker",
                    "displayLabel": "What was the time of the image capture?",
                    "required": true
                    },{
                    "id": "problem_restore_date",
                    "order": 9,
                    "visibility": "deployment_from == Backup",
                    "controlType": "datetimepicker",
                    "displayLabel": "What was the time of the attempted backup?",
                    "required": true
                    },{
                      "id": "problem_description",
                      "order": 10,
                      "controlType": "multilinetextbox",
                      "displayLabel": "Description",
                      "useAsAdditionalDetails": true,
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
