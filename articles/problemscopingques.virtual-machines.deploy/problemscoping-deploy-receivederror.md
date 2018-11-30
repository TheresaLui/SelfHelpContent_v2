<properties
                pageTitle="Cannot Deploy a Virtual Machine"
                description="Cannot Deploy a Virtual Machine"
                authors="tiag"
                authorAlias="summertgu"
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
                "formElements": [
                {
                  "id": "deployment_imagetype",
                  "order": 1,
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
                  "order": 2,
                  "controlType": "multilinetextbox",
                  "displayLabel": "What is the error you received?",
                  "required": false,
                  "useAsAdditionalDetails": true,
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
                      "value": "I do not know",
                      "text": "I do not know"
                      }
                      ],
                      "required": false
                  },{
                  "id": "correlation_id",
                  "order": 4,
                  "controlType": "textbox",
                  "displayLabel": "Correlation ID",
                  "useAsAdditionalDetails": false,
                  "required": false
                  },{
                  "id": "problem_description",
                  "order": 5,
                  "controlType": "multilinetextbox",
                  "displayLabel": "Description",
                  "useAsAdditionalDetails": false,
                  "required": true
                  }
                  ]
}
---
