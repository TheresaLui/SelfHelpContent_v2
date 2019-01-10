<properties
                pageTitle="Cannot Deploy a Virtual Machine"
                description="Cannot Deploy a Virtual Machine"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32628263"
                productPesIds="14749,15571,15797,16454,16470"
                cloudEnvironments="Public"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0040"
/>
# Deploy a VM
---
{
                "resourceRequired": true,
                "title": "My desired region or VM size is unavailable",
                "fileAttachmentHint": "",
                "formElements": [
                {
                  "id": "deployment_size",
                  "order": 1,
                  "controlType": "multilinetextbox",
                  "displayLabel": "What is the size of the VM you are trying to deploy?",
                  "required": false,
                  "useAsAdditionalDetails": true
                  },{
                    "id": "deployment_isinavailabilitysetzone",
                    "order": 2,
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
                  "id": "correlation_id",
                  "order": 3,
                  "controlType": "textbox",
                  "displayLabel": "Correlation ID",
                  "useAsAdditionalDetails": false,
                  "required": false
                  },{
                  "id": "problem_description",
                  "order": 4,
                  "controlType": "multilinetextbox",
                  "displayLabel": "Description",
                  "useAsAdditionalDetails": false,
                  "required": true
                  },{
                  "id": "problem_start_time",
                  "order": 5,
                  "controlType": "datetimepicker",
                  "displayLabel": "When did the problem start?",
                  "required": true
                }
                ]
}
---
