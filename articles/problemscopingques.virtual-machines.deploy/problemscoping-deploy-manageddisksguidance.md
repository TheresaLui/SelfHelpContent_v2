<properties
                pageTitle="Cannot Deploy a Virtual Machine"
                description="Cannot Deploy a Virtual Machine"
                authors="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32411844"
                productPesIds="14749"
                cloudEnvironments="Public"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea1212"
/>
# Deploy a VM
---
{
                "resourceRequired": true,
                "title": "I need guidance deploying with managed disks",
                "fileAttachmentHint": "",
                "formElements": [{
                  "id": "problem_end_date",
                  "order": 1,
                  "controlType": "datetimepicker",
                  "displayLabel": "When was the last reported time of the problem?",
                  "required": false
                  },{
                  "id": "deployment_item",
                  "order": 2,
                  "controlType": "dropdown",
                  "displayLabel": "Are you trying to create a managed OS disk, a managed data disk or a VM?",
                  "watermarkText": "Choose an option",
                  "dropdownOptions": [{
                    "value": "Managed OS disk",
                    "text": "Managed OS disk"
                    },{
                      "value": "Managed data disk",
                      "text": "Managed data disk"
                      },{
                        "value": "Virtual machine",
                        "text": "Virtual machine"
                      }
                      ],
                      "required": false
                      },{
                        "id": "deployment_vhdsnapshot",
                        "order": 3,
                        "controlType": "dropdown",
                        "displayLabel": "Are you creating from a VHD file or a snapshot?",
                        "watermarkText": "Choose an option",
                        "dropdownOptions": [{
                          "value": "VHD file",
                          "text": "VHD file"
                          },{
                            "value": "Snapshot",
                            "text": "Snapshot"
                            }
                            ],
                            "required": false
                          }
                          ]
}
---
