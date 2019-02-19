<properties
                pageTitle="Cannot Deploy a Virtual Machine"
                description="Cannot Deploy a Virtual Machine"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32628272"
                productPesIds="14749,15571,15797,16454,16470"
                cloudEnvironments="Public"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0036"
/>
# Deploy a VM
---
{
                "resourceRequired": true,
                "title": "I need guidance preparing an image",
                "fileAttachmentHint": "",
                "formElements": [
                {
                  "id": "resourceGroup",
                  "order": 1,
                  "controlType": "dropdown",
                  "displayLabel": "Select Deployment Failed Resource Group",
                  "dynamicDropdownOptions": {
                  "uri": "/subscriptions/{subscriptionId}/resourcegroups?api-version=2018-05-01",
                  "jTokenPath": "value",
                  "textProperty": "id",
                  "valueProperty": "id",
                  "textPropertyRegex": "[^/]+$"
                  },
                  "dropdownOptions": [{
                  "value": "Unable to retrieve list of Resource Groups",
                  "text": "Unable to retrieve list of Resource Groups."
                  }
                  ],
                  "useAsAdditionalDetails": false,
                  "required": true
                  },{
                  "id": "correlationId",
                  "order": 2,
                  "visibility": "resourceGroup != null",
                  "controlType": "dropdown",
                  "displayLabel": "Select Deployment Failure",
                  "dynamicDropdownOptions": {
                  "dependsOn": "resourceGroup",
                  "uri": "/subscriptions/{subscriptionId}/resourcegroups/{resourceGroup}/providers/Microsoft.Resources/deployments/?api-version=2018-05-01&$filter=provisioningState%20eq%20'Failed'&$top=10",
                  "jTokenPath": "value",
                  "textProperty": "properties.timestamp,properties.parameters.location.value,name",
                  "textTemplate":"Time:{properties.timestamp} Region:{properties.parameters.location.value} Name:{name}",
                  "valueProperty": "properties.correlationId",
                  "defaultDropdownOptions": {
                  "value": "Deployment Failure not found",
                  "text": "Deployment Failure not found",
                  },
                  "textPropertyRegex": "[^/]+$"
                  },
                  "dropdownOptions": [{
                  "value": "Unable to retrieve list of Deployment Failure",
                  "text": "Unable to retrieve list of Deployment Failure."
                  }
                  ],
                  "useAsAdditionalDetails": false,
                  "required": false
                  },{
                  "id": "deployment_os",
                  "order": 3,
                  "controlType": "multilinetextbox",
                  "displayLabel": "What is the distribution and version of OS?",
                  "required": false,
                  "useAsAdditionalDetails": true
                  },{
                  "id": "problem_description",
                  "order": 4,
                  "controlType": "multilinetextbox",
                  "displayLabel": "Description",
                  "useAsAdditionalDetails": false,
                  "required": true
                  },{
                  "id": "problem_start_time",
                  "order": 5,
                  "controlType": "datetimepicker",
                  "displayLabel": "When did the problem start?",
                  "required": true
                }
                ]
}
---
