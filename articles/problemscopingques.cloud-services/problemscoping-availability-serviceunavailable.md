<properties
                pageTitle="Application and Service Availability"
                description="Application and Service Availability"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32591241"
                productPesIds="13185"
                cloudEnvironments="Public"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0098"
/>
# Availability
---
{
                "resourceRequired": true,
                "title": "Service was or is unavailable",
                "fileAttachmentHint": "",
                "formElements": [
                {
                    "id": "problem_start_time",
                    "order": 1,
                    "controlType": "datetimepicker",
                    "displayLabel": "Start time of most recent occurrence",
                    "required": true
                },{
                    "id": "unavailable_symptoms",
                    "order": 2,
                    "controlType": "multilinetextbox",
                    "displayLabel": "What were the exact symptoms during the time the service was unavailable?",
                    "required": false,
                    "useAsAdditionalDetails": false
                },{
                      "id": "iis_logs",
                      "order": 3,
                      "controlType": "dropdown",
                      "displayLabel": "Have you checked the IIS logs on the role instances during this time? If yes, please upload the IIS logs corresponding to this time.",
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
                      "id": "if_external_monitoring",
                      "order": 4,
                      "controlType": "dropdown",
                      "displayLabel": "Do you have any external monitoring/logging in your code/performance counters that were high during this time?",
                      "watermarkText": "Choose an option",
                      "dropdownOptions": [
                        {
                          "value": "Yes (specify below)",
                          "text": "Yes (specify below)"
                        },{
                          "value": "No",
                          "text": "No"
                        }
                        ],
                        "required": false
                  },{
                  "id": "problem_description",
                  "order": 5,
                  "controlType": "multilinetextbox",
                  "displayLabel": "Description",
                  "useAsAdditionalDetails": true,
                  "required": true
                  }
                ]
}
---
