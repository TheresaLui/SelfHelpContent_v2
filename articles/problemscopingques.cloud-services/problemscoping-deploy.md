<properties
                pageTitle="Deployment"
                description="Deployment"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32565474,32565476,32565478,32565479,32591243"
                productPesIds="13185"
                cloudEnvironments="Public"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0101"
/>
# Deployment
---
{
                "resourceRequired": true,
                "fileAttachmentHint": "",
                "formElements": [
                {
                    "id": "deploy_error",
                    "order": 1,
                    "controlType": "multilinetextbox",
                    "displayLabel": "What is the error you received?",
                    "required": false,
                    "useAsAdditionalDetails": false
                },{
                    "id": "correlation_id",
                    "order": 2,
                    "controlType": "textbox",
                    "displayLabel": "What is the Correlation ID or Operation ID corresponding to the failure?",
                    "required": false
                },{
                    "id": "deploy_from",
                    "order": 3,
                    "controlType": "dropdown",
                    "displayLabel": "From where you deployed your cloud service?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                      {
                        "value": "Visual Studio",
                        "text": "Visual Studio"
                      },{
                        "value": "PowerShell",
                        "text": "PowerShell"
                      },{
                        "value": "Portal",
                        "text": "Portal"
                      }
                      ],
                      "required": false
                  },{
                  "id": "problem_description",
                  "order": 4,
                  "controlType": "multilinetextbox",
                  "displayLabel": "Description",
                  "useAsAdditionalDetails": true,
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
