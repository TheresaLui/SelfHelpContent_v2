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
                "title": "My desired region or VM size is unavailable",
                "fileAttachmentHint": "",
                "formElements": [{
                  "id": "problem_end_date",
                  "order": 1,
                  "controlType": "datetimepicker",
                  "displayLabel": "When was the last reported time of the problem?",
                  "required": false
                },{
                  "id": "deployment_size",
                  "order": 2,
                  "controlType": "multilinetextbox",
                  "displayLabel": "What is the size of the VM you are trying to deploy?",
                  "required": false,
                  "useAsAdditionalDetails": true,
                  "hints": [{
                    "text": "Size of the virtual machine you are trying to deploy."
                    }]
                  },{
                    "id": "deployment_isinavailabilityset",
                    "order": 3,
                    "controlType": "dropdown",
                    "displayLabel": "Are you deploying your VM in an availability set?",
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
                  }
                  ]
}
---
