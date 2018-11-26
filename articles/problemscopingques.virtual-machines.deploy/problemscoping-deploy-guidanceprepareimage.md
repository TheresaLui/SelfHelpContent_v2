<properties
                pageTitle="Cannot Deploy a Virtual Machine"
                description="Cannot Deploy a Virtual Machine"
                authors="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32628272"
                productPesIds="14749"
                cloudEnvironments="Public"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea1212"
/>
# Deploy a VM
---
{
                "resourceRequired": true,
                "title": "I need guidance preparing an image",
                "fileAttachmentHint": "",
                "formElements": [{
                  "id": "problem_end_date",
                  "order": 1,
                  "controlType": "datetimepicker",
                  "displayLabel": "When was the last reported time of the problem?",
                  "required": false
                  },{
                  "id": "deployment_os",
                  "order": 2,
                  "controlType": "multilinetextbox",
                  "displayLabel": "What is the distribution and version of OS?",
                  "required": false,
                  "useAsAdditionalDetails": true,
                  "hints": [{
                    "text": "Distribution and version of the operating system."
                    }]
                  },{
                  "id": "deployment_isfollowingchecklist",
                  "order": 3,
                  "controlType": "dropdown",
                  "displayLabel": "Have you followed <a href='https://docs.microsoft.com/azure/virtual-machines/windows/prepare-for-upload-vhd-image'>the checklist for uploading a VM</a>?",
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
                    }
                    ]
}
---
