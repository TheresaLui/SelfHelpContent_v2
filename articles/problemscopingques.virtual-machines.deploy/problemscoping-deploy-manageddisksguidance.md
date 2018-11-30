<properties
                pageTitle="Cannot Deploy a Virtual Machine"
                description="Cannot Deploy a Virtual Machine"
                authors="tiag"
                authorAlias="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32628271"
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
                "formElements": [
                {
                  "id": "deployment_item",
                  "order": 1,
                  "controlType": "dropdown",
                  "displayLabel": "Which type of disk are you trying to create?",
                  "watermarkText": "Choose an option",
                  "dropdownOptions": [{
                    "value": "Managed OS disk",
                    "text": "Managed OS disk"
                    },{
                      "value": "Managed data disk",
                      "text": "Managed data disk"
                      }
                      ],
                      "required": false
                      },{
                        "id": "deployment_from",
                        "order": 2,
                        "controlType": "dropdown",
                        "displayLabel": "What are you trying to create from?",
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
                  "order": 3,
                  "visibility": "deployment_from == Snapshot",
                  "controlType": "datetimepicker",
                  "displayLabel": "When was the time of the attempted snapshot?",
                  "required": true
                  },{
                  "id": "problem_caputre_date",
                  "order": 4,
                  "visibility": "deployment_from == Captured image",
                  "controlType": "datetimepicker",
                  "displayLabel": "When was the time of the image capture?",
                  "required": true
                  },{
                  "id": "problem_restore_date",
                  "order": 5,
                  "visibility": "deployment_from == Backup",
                  "controlType": "datetimepicker",
                  "displayLabel": "When was the time of the attempted backup?",
                  "required": true
                  },{
                  "id": "correlation_id",
                  "order": 6,
                  "controlType": "textbox",
                  "displayLabel": "Correlation ID",
                  "useAsAdditionalDetails": false,
                  "required": false
                  },{
                  "id": "problem_description",
                  "order": 7,
                  "controlType": "multilinetextbox",
                  "displayLabel": "Description",
                  "useAsAdditionalDetails": false,
                  "required": true
                  }
                  ]
}
---
