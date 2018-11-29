<properties
                pageTitle="Cannot Deploy a Virtual Machine"
                description="Cannot Deploy a Virtual Machine"
                authors="tiag"
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
                "formElements": [{
                  "id": "problem_end_date",
                  "order": 1,
                  "controlType": "datetimepicker",
                  "displayLabel": "When was the last reported time of the problem?",
                  "required": true
                    },{
                        "id": "deployment_vhdsnapshot",
                        "order": 2,
                        "controlType": "dropdown",
                        "displayLabel": "Are you creating from a VHD file, a snapshot, or a captured image?",
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
                            }
                            ],
                            "required": false
                          }
                        ]
}
---
