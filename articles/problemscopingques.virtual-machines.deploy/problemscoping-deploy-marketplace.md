<properties
                pageTitle="Cannot Deploy a Virtual Machine"
                description="Cannot Deploy a Virtual Machine"
                authors="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32628274"
                productPesIds="14749"
                cloudEnvironments="Public"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea1212"
/>
# Deploy a VM
---
{
                "resourceRequired": true,
                "title": "Troubleshoot marketplace image deployment failures",
                "fileAttachmentHint": "",
                "formElements": [
                {
                  "id": "deployment_marketplaceimage",
                  "order": 1,
                  "controlType": "multilinetextbox",
                  "displayLabel": "What marketplace image are you trying to deploy? ",
                  "required": false,
                  "useAsAdditionalDetails": true,
                  "hints": [{
                    "text": "Name of the marketplace image you are trying to deploy."
                    }]
                  },{
                        "id": "is_publisher",
                        "order": 2,
                        "controlType": "dropdown",
                        "displayLabel": "Are you a publisher of this image?",
                        "watermarkText": "Choose an option",
                        "dropdownOptions": [{
                          "value": "Yes",
                          "text": "Yes"
                          },{
                            "value": "No",
                            "text": "No"
                          }
                          ],
                          required": false
                  },{
                  "id": "correlation_id",
                  "order": 3,
                  "controlType": "textbox",
                  "displayLabel": "Correlation ID",
                  "useAsAdditionalDetails": false,
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
