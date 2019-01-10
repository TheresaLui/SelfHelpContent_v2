<properties
                pageTitle="Virtual Machine Extensions not operating correctly"
                description="Virtual Machines Extensions not operating correctly"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32628256"
                productPesIds="14749,15571,15797,16454,16470"
                cloudEnvironments="Public"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0043"
/>
# Agent and extensions
---
{
                "resourceRequired": true,
                "title": "Azure Custom Script (CSE) extension issue",
                "fileAttachmentHint": "",
                "formElements": [
                {
                  "id": "extension_error",
                  "order": 1,
                  "controlType": "multilinetextbox",
                  "displayLabel": "What is the error you received?",
                  "required": false,
                  "useAsAdditionalDetails": true
                },{
                    "id": "extension_operation",
                    "order": 2,
                    "controlType": "dropdown",
                    "displayLabel": "What operation are you trying to do?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [{
                      "value": "Install",
                      "text": "Install"
                      },{
                      "value": "Uninstall",
                      "text": "Uninstall"
                      },{
                      "value": "Enable",
                      "text": "Enable"
                      },{
                      "value": "Troubleshoot",
                      "text": "Troubleshoot"
                      },{
                      "value": "I do not know",
                      "text": "I do not know"
                      }
                      ],
                      "required": false
                },{
                      "id": "extension_scriptlink",
                      "order": 3,
                      "controlType": "multilinetextbox",
                      "displayLabel": "What custom script are you trying to run? Paste script or provide link if it is publicly available.",
                      "useAsAdditionalDetails": true,
                      "required": true
                },{
                    "id": "extension_agentinstalled",
                    "order": 4,
                    "controlType": "dropdown",
                    "displayLabel": "Do you have the latest Azure VM Agent installed?",
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
                    "id": "extension_agentinstalled",
                    "order": 5,
                    "controlType": "dropdown",
                    "displayLabel": "Do you have the latest Azure VM Agent installed?",
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
                  "order": 6,
                  "controlType": "multilinetextbox",
                  "displayLabel": "Description",
                  "useAsAdditionalDetails": false,
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
