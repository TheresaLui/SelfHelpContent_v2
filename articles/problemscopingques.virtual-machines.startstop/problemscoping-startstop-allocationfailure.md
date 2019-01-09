<properties
                pageTitle="Cannot Start or Stop My Virtual Machine"
                description="Cannot Start or Stop My Virtual Machine"
                authors="summertgu"
                authorAlias="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32628253"
                productPesIds="14749,15571,15797,16454,16470"
                cloudEnvironments="Public"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0007"
/>
# Start or Stop My VM
---
{
                "resourceRequired": true,
                "title": "I received an allocation failure",
                "fileAttachmentHint": "",
                "formElements": [
                {
                    "id": "startstop_operation",
                    "order": 1,
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
                    "id": "startstop_isinavailabilitysetzone",
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
                  "id": "startstop_isinscaleset",
                  "order": 3,
                  "controlType": "dropdown",
                  "displayLabel": "Are you deploying your VM in a scale set?",
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
                  "useAsAdditionalDetails": true,
                  "required": true
                  },{
                  "id": "problem_start_time",
                  "order": 6,
                  "controlType": "datetimepicker",
                  "displayLabel": "When did the problem start?",
                  "required": true
                }
                ]
}
---
