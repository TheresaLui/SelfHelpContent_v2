<properties
                pageTitle="My Virtual Machine restarted, paused, or stopped unexpectedly"
                description="My Virtual Machine restarted, paused, or stopped unexpectedly"
                authors="summertgu"
                authorAlias="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32628287"
                productPesIds="15571,15797,16454,16470"
                cloudEnvironments="Public"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0000"
/>
# VM Restart
---
{
                "resourceRequired": true,
                "title": "Help diagnose my VM restart issue",
                "fileAttachmentHint": "",
                "formElements": [
                {
                "id": "restart_error",
                "order": 1,
                "controlType": "multilinetextbox",
                "displayLabel": "What is the error you received?",
                "required": false,
                "useAsAdditionalDetails": true
                },{
                      "id": "machinetype",
                      "order": 2,
                      "controlType": "dropdown",
                      "displayLabel": "Which machine version are you running?",
                      "watermarkText": "Choose an option",
                      "dropdownOptions": [
                      {
                        "value": "Ubuntu",
                        "text": "Ubuntu"
                      },
                      {
                        "value": "Redhat",
                        "text": "Redhat"
                      },
                      {
                        "value": "Other",
                        "text": "Other"
                      }
                      ],
                      "required": false
                  },{
                  "id": "problem_description",
                  "order": 3,
                  "controlType": "multilinetextbox",
                  "displayLabel": "Description",
                  "useAsAdditionalDetails": false,
                  "required": true
                  },{
                  "id": "problem_start_time",
                  "order": 4,
                  "controlType": "datetimepicker",
                  "displayLabel": "When did the problem start?",
                  "required": true
                }
                ]
}
---
