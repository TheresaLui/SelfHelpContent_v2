<properties
                pageTitle="Management"
                description="Management"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32449676"
                productPesIds="10680"
                cloudEnvironments="Public"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0111"
/>
# Management
---
{
    "resourceRequired": true,
    "title": "Cannot stop, start, delete, or restart VM Scale Sets",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "startstop_error",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the error you received?",
            "required": false,
            "useAsAdditionalDetails": false
        },{
            "id": "startstop_operation",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What operation are you trying to do?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [{
              "value": "Start",
              "text": "Start"
              },{
              "value": "Stop",
              "text": "Stop"
              },{
              "value": "Delete",
              "text": "Delete"
              },{
              "value": "Restart",
              "text": "Restart"
              }
              ],
              "required": false
          },{
              "id": "startstop_previous",
              "order": 3,
              "controlType": "dropdown",
              "displayLabel": "Has this operation worked previously for this VMSS?",
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
            "id": "startstop_config",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "What was your configuration change prior to the issue starting?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "I resized my virtual machine scale set",
                    "text": "I resized my virtual machine scale set"
                },
                {
                    "value": "I attached or detached disks",
                    "text": "I attached or detached disks"
                },
                {
                    "value": "I moved my VM to another network/subnet or resource group",
                    "text": "I moved my VM to another network/subnet or resource group"
                },
                {
                    "value": "I changed my firewall configuration",
                    "text": "I changed my firewall configuration"
                },
                {
                    "value": "I installed a third party application",
                    "text": "I installed a third party application"
                },
                {
                    "value": "Other",
                    "text": "Other"
                }
            ],
            "required": false
        },
        {
            "id": "startstop_config_other",
            "order": 5,
            "visibility": "startstop_config == Other",
            "controlType": "multilinetextbox",
            "displayLabel": "Please specify your configuration change prior to the issue starting.",
            "required": false,
            "useAsAdditionalDetails": false
        },
        {
            "id": "startstop_ifnew",
            "order": 6,
            "controlType": "dropdown",
            "displayLabel": "Is this VMSS new to Azure?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "I do not know",
                    "text": "I do not know"
                }
            ],
            "required": false
        },
        {
            "id": "startstop_ifbackup",
            "order": 7,
            "controlType": "dropdown",
            "displayLabel": "Was this VMSS recovered from backup?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "I do not know",
                    "text": "I do not know"
                }
            ],
            "required": false
        },
        {
            "id": "startstop_ifinternet",
            "order": 8,
            "controlType": "dropdown",
            "displayLabel": "Do you have Internet connectivity issues from this VMSS?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 9,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 10,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ]
}
---
