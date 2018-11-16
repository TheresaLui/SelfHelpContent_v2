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
                "title": "I received an allocation failure",
                "fileAttachmentHint": "",
                "formElements": [{
                  "id": "problem_end_date",
                  "order": 1,
                  "controlType": "datetimepicker",
                  "displayLabel": "When was the last reported time of the problem?",
                  "required": false
                },{
                    "id": "create_or_resize",
                    "order": 2,
                    "controlType": "dropdown",
                    "displayLabel": "Are you trying to create or resize the VM?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [{
                      "value": "Create",
                      "text": "Create"
                      },{
                        "value": "Resize",
                        "text": "Resize"
                        }
                        ],
                        "required": false
                  },{
                    "id": "deployment_scenario",
                    "order": 3,
                    "controlType": "dropdown",
                    "displayLabel": "Which of the following describes your scenario?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [{
                      "value": "Restart partially stopped (deallocated) VMs",
                      "text": "Restart partially stopped (deallocated) VMs"
                      },{
                        "value": "Resize a VM or add VMs to an existing availability set",
                        "text": "Resize a VM or add VMs to an existing availability set"
                      },{
                        "value": "Restart fully stopped (deallocated) VMs",
                        "text": "Restart fully stopped (deallocated) VMs"
                      },{
                        "value": "Allocation failures for older VM sizes",
                        "text": "Allocation failures for older VM sizes"
                        }
                        ],
                        "required": false
                  }
                ]
}
---
