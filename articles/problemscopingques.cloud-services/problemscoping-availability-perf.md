<properties
                pageTitle="Application and Service Availability"
                description="Application and Service Availability"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32422588"
                productPesIds="13185"
                cloudEnvironments="Public"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0097"
/>
# Availability
---
{
                "resourceRequired": true,
                "title": "Performance",                
                "fileAttachmentHint": "",
                "formElements": [
                {
                    "id": "problem_start_time",
                    "order": 1,
                    "controlType": "datetimepicker",
                    "displayLabel": "Start time of most recent occurrence",
                    "required": true
                },{
                    "id": "slowness_second",
                    "order": 2,
                    "controlType": "textbox",
                    "displayLabel": "How much is the slowness (in seconds)?",
                    "required": false
                },{
                    "id": "occurrence_pattern",
                    "order": 3,
                    "controlType": "dropdown",
                    "displayLabel": "What is the pattern of occurrence of the issue?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                      {
                        "value": "Intermittent",
                        "text": "Intermittent"
                      },{
                        "value": "Consistent",
                        "text": "Consistent"
                      },{
                        "value": "During high load",
                        "text": "During high load"
                      },{
                        "value": "During a specific time of the day",
                        "text": "During a specific time of the day"
                      }
                      ],
                      "required": false
                  },{
                      "id": "cpu_util",
                      "order": 4,
                      "controlType": "multilinetextbox",
                      "displayLabel": "What is CPU / Memory / Disk / Network Utilization during the time of the issue?",
                      "required": false,
                      "useAsAdditionalDetails": false
                  },{
                      "id": "mitigation_steps",
                      "order": 5,
                      "controlType": "dropdown",
                      "displayLabel": "What mitigation steps do you take to overcome the issue?",
                      "watermarkText": "Choose an option",
                      "dropdownOptions": [
                        {
                          "value": "The problem resolves itself on its own",
                          "text": "The problem resolves itself on its own"
                        },{
                          "value": "I have to recycle IIS/Reboot the instance to resolve the problem",
                          "text": "I have to recycle IIS/Reboot the instance to resolve the problem"
                        },{
                          "value": "Other (describe below)",
                          "text": "Other (describe below)"
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
                  }
                ]
}
---
