<properties
                pageTitle="Identity/Service Principal related"
                description="Identity/Service Principal related"
                authors="ChiragPavecha"
                ms.author="chiragpa"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32637212"
                productPesIds="16450"
                cloudEnvironments="Public"
                schemaVersion="1"
                articleId="problemscoping-identity-spn"
/>
# Service Principal related
---
{
                "subscriptionRequired": true,
                "resourceRequired": true,
                "title": "Service Principal related",
                "fileAttachmentHint": "",
                "formElements": [
                 {
                    "id": "problem_start_time",
                    "order": 1,
                    "controlType": "datetimepicker",
                    "displayLabel": "When did the problem start?",
                    "required": true
                },
                {
                    "id": "getErrorMsg",
                    "order": 2,
                    "controlType": "multilinetextbox",
                    "displayLabel": "What error message did you receive while performing this operation, if any?",
                    "required": false
                  },
                  {
                    "id": "getGlobalAdmin",
                     "order": 3,
                      "controlType": "dropdown",
                      "displayLabel": "Is the user that created the server and client applications a Global Admin for the AD tenant?",
                      "watermarkText": "Choose an option",
                      "dropdownOptions": [
                        {
                          "value": "Yes",
                          "text": "Yes"
                        },{
                          "value": "No",
                          "text": "No"
                        },
                        {
                          "value": "dont_know_answer",
                          "text": "I don't know"
                        }
                        ],
                        "required": false
                  },
                  {
                    "id": "getAdminFlagWork",
                     "order": 4,
                      "controlType": "dropdown",
                      "displayLabel": "Does using **az aks get-credentials** with the **--admin** flag work as expected",
                      "watermarkText": "Choose an option",
                      "dropdownOptions": [
                        {
                          "value": "Yes",
                          "text": "Yes"
                        },{
                          "value": "No",
                          "text": "No"
                        },
                        {
                          "value": "dont_know_answer",
                          "text": "I don't try"
                        }
                        ],
                        "required": false
                  },
                  {
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
