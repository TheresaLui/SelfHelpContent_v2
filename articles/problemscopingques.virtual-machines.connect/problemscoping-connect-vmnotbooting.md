<properties
                pageTitle="Cannot Connect to My Virtual Machine"
                description="Cannot Connect to My Virtual Machine"
                authors="tiag"
                authorAlias="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32615532"
                productPesIds="14749"
                cloudEnvironments="Public"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea1212"
/>
# Connect to a VM
---
{
                "resourceRequired": true,
                "title": "My VM is not booting",
                "fileAttachmentHint": "",
                "formElements": [
                {
                "id": "connect_error",
                "order": 1,
                "controlType": "multilinetextbox",
                "displayLabel": "What is the error you received?",
                "required": false,
                "useAsAdditionalDetails": true,
                "hints": [{
                  "text": "Copy and paste the specific error from the activity log."
                  }]
                },{
                    "id": "connect_request",
                    "order": 2,
                    "controlType": "dropdown",
                    "displayLabel": "What do you need help with?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [{
                      "value": "Mitigate my non-booting problem",
                      "text": "Mitigate my non-booting problem"
                      },{
                      "value": "Recreate the Virtual Machine",
                      "text": "Recreate the Virtual Machine"
                      },{
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
                  }
                  ]
}
---
