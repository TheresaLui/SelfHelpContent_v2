<properties
                pageTitle="Cannot Start or Stop My Virtual Machine"
                description="Cannot Start or Stop My Virtual Machine"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32628286"
                productPesIds="14749,15571,15797,16454,16470"
                cloudEnvironments="Public"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0012"
/>
# Start or Stop My VM
---
{
                "resourceRequired": true,
                "title": "My VM is unresponsive to start or stop operations",
                "fileAttachmentHint": "",
                "formElements": [
                {
                "id": "startstop_error",
                "order": 1,
                "controlType": "multilinetextbox",
                "displayLabel": "What is the error you received?",
                "required": false,
                "useAsAdditionalDetails": false,
                },{
                    "id": "startstop_previous",
                    "order": 2,
                    "controlType": "dropdown",
                    "displayLabel": "Has this operation worked previously for this VM?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [{
                      "value": "Yes",
                      "text": "Yes"
                      },{
                      "value": "No",
                      "text": "No"
                      },{
                      "value": "I do not know",
                      "text": "I do not know"
                      }
                      ],
                      "required": false
              },{
                  "id": "problem_description",
                  "order": 3,
                  "controlType": "multilinetextbox",
                  "displayLabel": "Description",
                  "useAsAdditionalDetails": true,
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
