<properties
                pageTitle="Configuration and Management"
                description="Configuration and Management"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32569897"
                productPesIds="13185"
                cloudEnvironments="Public"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0100"
/>
# Config and Management
---
{
                "resourceRequired": true,
                "title": "Scaling",
                "fileAttachmentHint": "",
                "formElements": [
                {
                    "id": "scaling_error",
                    "order": 1,
                    "controlType": "multilinetextbox",
                    "displayLabel": "What is the error you received?",
                    "required": false,
                    "useAsAdditionalDetails": false
                },{
                    "id": "scale_setting",
                    "order": 2,
                    "controlType": "multilinetextbox",
                    "displayLabel": "What is your current scale setting?",
                    "required": false,
                    "useAsAdditionalDetails": false
                },{
                    "id": "scale_resource",
                    "order": 3,
                    "controlType": "textbox",
                    "displayLabel": "What resource are you trying to scale?",
                    "required": false
                },{
                    "id": "scale_other_resource",
                    "order": 4,
                    "controlType": "dropdown",
                    "displayLabel": "Are you having the same issues on other resources?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                      {
                        "value": "Yes",
                        "text": "Yes"
                      },{
                        "value": "No",
                        "text": "No"
                      }
                      ],
                      "required": false
                  },{
                      "id": "autoscaling",
                      "order": 5,
                      "controlType": "dropdown",
                      "displayLabel": "What kind of customer autoscaling you are using?",
                      "watermarkText": "Choose an option",
                      "dropdownOptions": [
                        {
                          "value": "I am using a tool that manages my autoscaling using the Azure rest APIs",
                          "text": "I am using a tool that manages my autoscaling using the Azure rest APIs"
                        },{
                          "value": "I am using Azure autoscaling through Azure portal",
                          "text": "I am using Azure autoscaling through Azure portal"
                        }
                        ],
                        "required": false
                  },{
                  "id": "problem_description",
                  "order": 6,
                  "controlType": "multilinetextbox",
                  "displayLabel": "Description",
                  "useAsAdditionalDetails": true,
                  "required": true
                  },{
                  "id": "problem_start_time",
                  "order": 7,
                  "controlType": "datetimepicker",
                  "displayLabel": "When did the problem start?",
                  "required": true
                }
                ]
}
---
