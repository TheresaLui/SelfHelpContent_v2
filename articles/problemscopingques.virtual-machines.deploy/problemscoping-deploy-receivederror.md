<properties
                pageTitle="Cannot Deploy a Virtual Machine"
                description="Cannot Deploy a Virtual Machine"
                authors="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32628279"
                productPesIds="14749"
                cloudEnvironments="Public"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea1212"
/>
# Deploy a VM
---
{
                "resourceRequired": true,
                "title": "I received a provisioning or deployment timeout error",
                "fileAttachmentHint": "",
                "formElements": [{
                  "id": "problem_end_date",
                  "order": 1,
                  "controlType": "datetimepicker",
                  "displayLabel": "When was the last reported time of the problem?",
                  "required": true
                },{
                  "id": "deployment_imagetype",
                  "order": 2,
                  "controlType": "dropdown",
                  "displayLabel": "Choose the type of image deployment",
                  "watermarkText": "Choose an option",
                  "dropdownOptions": [{
                    "value": "Custom Image",
                    "text": "Custom Image"
                    },{
                      "value": "Marketplace Image",
                      "text": "Marketplace Image"
                      },{
                        "value": "I do not know",
                        "text": "I do not know"
                      }
                      ],
                      "required": false
                      },{
                  "id": "deployment_error",
                  "order": 3,
                  "controlType": "multilinetextbox",
                  "displayLabel": "What is the error you received?",
                  "required": false,
                  "useAsAdditionalDetails": true,
                  "hints": [{
                    "text": "Copy and paste the specific error from the activity log."
                    }]
                  },{
                  "id": "problem_description",
                  "order": 4,
                  "controlType": "multilinetextbox",
                  "displayLabel": "Description",
                  "required": true
                  }
                  ]
}
---
