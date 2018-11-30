<properties
                pageTitle="Cannot Connect to My Virtual Machine"
                description="Cannot Connect to My Virtual Machine"
                authors="tiag"
                authorAlias="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32615530"
                productPesIds="14749"
                cloudEnvironments="Public"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea1212"
/>
# Connect to a VM
---
{
                "resourceRequired": true,
                "title": "My configuration change impacted connectivity",
                "fileAttachmentHint": "",
                "formElements": [
                {
                "id": "connect_error",
                "order": 1,
                "controlType": "multilinetextbox",
                "displayLabel": "What is the error you received?",
                "required": false,
                "useAsAdditionalDetails": false,
                "hints": [{
                  "text": "Copy and paste the specific error from the activity log."
                  }]
                },{
                "id": "connect_config",
                "order": 2,
                "controlType": "multilinetextbox",
                "displayLabel": "What was your configuration change prior to the issue started?",
                "required": false,
                "useAsAdditionalDetails": true,
                },{
                    "id": "connect_ifmigrated",
                    "order": 3,
                    "controlType": "dropdown",
                    "displayLabel": "Was this VM just migrated?",
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
                },{
                  "id": "problem_description",
                  "order": 4,
                  "controlType": "multilinetextbox",
                  "displayLabel": "Description",
                  "useAsAdditionalDetails": false,
                  "required": true
                  }
                  ]
}
---
