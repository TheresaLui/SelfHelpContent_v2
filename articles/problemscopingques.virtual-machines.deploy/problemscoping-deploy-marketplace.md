<properties
                pageTitle="Cannot Deploy a Virtual Machine"
                description="Cannot Deploy a Virtual Machine"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32628274"
                productPesIds="14749,15571,15797,16454,16470"
                cloudEnvironments="Public"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0038"
/>
# Deploy a VM
---
{
                "resourceRequired": true,
                "title": "Troubleshoot Marketplace image deployment failures",
                "fileAttachmentHint": "",
                "formElements": [
                {
                  "id": "resourceGroup",
                  "order": 1,
                  "controlType": "dropdown",
                  "displayLabel": "Select resource group for deployment failure",
                  "dynamicDropdownOptions": {
                  "uri": "/subscriptions/{subscriptionId}/resourcegroups?api-version=2018-05-01",
                  "jTokenPath": "value",
                  "textProperty": "id",
                  "valueProperty": "id",
                  "textPropertyRegex": "[^/]+$"
                  },
                  "dropdownOptions": [{
                  "value": "Unable to retrieve list of resource groups.",
                  "text": "Unable to retrieve list of resource groups."
                  }
                  ],
                  "useAsAdditionalDetails": false,
                  "required": true
                  },{
                  "id": "correlationId",
                  "order": 2,
                  "visibility": "resourceGroup != null",
                  "controlType": "dropdown",
                  "displayLabel": "Select failed deployment",
                  "dynamicDropdownOptions": {
                  "dependsOn": "resourceGroup",
                  "uri": "/subscriptions/{subscriptionId}/resourcegroups/{resourceGroup}/providers/Microsoft.Resources/deployments/?api-version=2018-05-01&$filter=provisioningState%20eq%20'Failed'&$top=10",
                  "jTokenPath": "value",
                  "textProperty": "properties.timestamp,properties.parameters.location.value,name",
                  "textTemplate":"Time:{properties.timestamp} Region:{properties.parameters.location.value} Name:{name}",
                  "valueProperty": "properties.correlationId",
                  "defaultDropdownOptions": {
                  "value": "Deployment failure not found.",
                  "text": "Deployment failure not found."
                  },
                  "textPropertyRegex": "[^/]+$"
                  },
                  "dropdownOptions": [{
                  "value": "Unable to retrieve list of failed deployments.",
                  "text": "Unable to retrieve list of failed deployments."
                  }
                  ],
                  "useAsAdditionalDetails": false,
                  "required": false
                  },{
                  "id": "deployment_marketplaceimage",
                  "order": 3,
                  "controlType": "multilinetextbox",
                  "displayLabel": "What Marketplace image are you trying to deploy?",
                  "useAsAdditionalDetails": true,
                  "required": false
                },{
                  "id": "is_publisher",
                  "order": 4,
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
                      "required": false
                },{
                  "id": "problem_description",
                  "order": 5,
                  "controlType": "multilinetextbox",
                  "displayLabel": "Description",
                  "useAsAdditionalDetails": false,
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
