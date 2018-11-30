<properties
                pageTitle="Cannot Deploy a Virtual Machine"
                description="Cannot Deploy a Virtual Machine"
                authorAlias="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32628252"
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
                "formElements": [
                {
                    "id": "deployment_operation",
                    "order": 1,
                    "controlType": "dropdown",
                    "displayLabel": "What is the operation you are trying to do?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [{
                      "value": "Create",
                      "text": "Create"
                      }，{
                      "value": "Start",
                      "text": "Start"
                      },{
                      "value": "Resize",
                      "text": "Resize"
                      },{
                      "value": "Redeploy",
                      "text": "Redeploy"
                      },{
                      "value": "I don't know",
                      "text": "I don't know"
                      }
                      ],
                      "required": false
                  },{
                    "id": "deployment_scenario",
                    "order": 2,
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
                  },{
                    "id": "deployment_isinavailabilitysetzone",
                    "order": 3,
                    "controlType": "dropdown",
                    "displayLabel": "Are you deploying your VM in an availability set or zone?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [{
                      "value": "Yes",
                      "text": "Yes"
                      },{
                        "value": "No",
                        "text": "No"
                        }
                        ],
                        "required": false
                },{
                    "id": "deployment_operation",
                    "order": 4,
                    "controlType": "dropdown",
                    "displayLabel": "What operation are you trying to do?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [{
                      "value": "Create",
                      "text": "Create"
                      }，{
                      "value": "Start",
                      "text": "Start"
                      },{
                      "value": "Resize",
                      "text": "Resize"
                      },{
                      "value": "Redeploy",
                      "text": "Redeploy"
                      },{
                      "value": "I don't know",
                      "text": "I don't know"
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
