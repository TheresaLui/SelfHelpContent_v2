<properties
                pageTitle="Cannot Deploy a Virtual Machine"
                description="Cannot Deploy a Virtual Machine"
                authorAlias="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32628259"
                productPesIds="14749"
                cloudEnvironments="Public"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea1212"
/>
# Deploy a VM
---
{
                "resourceRequired": true,
                "title": "I am unable to deploy a captured or generalized image",
                "fileAttachmentHint": "",
                "formElements": [
                {
                        "id": "deployment_from",
                        "order": 1,
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
                  "order": 2,
                  "visibility": "deployment_from == Snapshot",
                  "controlType": "datetimepicker",
                  "displayLabel": "When was the time of the attempted snapshot?",
                  "required": true
                  },{
                  "id": "problem_caputre_date",
                  "order": 3,
                  "visibility": "deployment_from == Captured image",
                  "controlType": "datetimepicker",
                  "displayLabel": "When was the time of the image capture?",
                  "required": true
                  },{
                  "id": "problem_restore_date",
                  "order": 4,
                  "visibility": "deployment_from == Backup",
                  "controlType": "datetimepicker",
                  "displayLabel": "When was the time of the attempted backup?",
                  "required": true
                  },{
                  "id": "correlation_id",
                  "order": 5,
                  "controlType": "textbox",
                  "displayLabel": "Correlation ID",
                  "useAsAdditionalDetails": false,
                  "required": false
                  },{
                  "id": "problem_description",
                  "order": 6,
                  "controlType": "multilinetextbox",
                  "displayLabel": "Description",
                  "useAsAdditionalDetails": false,
                  "required": true
                  }
                  ]
}
---
