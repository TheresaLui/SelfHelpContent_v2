<properties
                pageTitle="Cannot Deploy a Virtual Machine"
                description="Cannot Deploy a Virtual Machine"
                authors="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32411844"
                productPesIds="14749"
                cloudEnvironments="Public"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea1212"
/>
# Deploy a VM
---
{
                "resourceRequired": true,
                "title": "I received an allocation failure",
                "fileAttachmentHint": "",
                "formElements": [{
                  "id": "selectfailedoperation",
                  "order": 1,
                  "controlType": "dropdown",
                  "displayLabel": "Please select the operation name you are experiencing a deployment failure with",
                  "watermarkText": "Choose an option",
                  "dynamicDropdownOptions": {
                    "uri": "/subscriptions/{subscriptionid}/resourceGroups/{resourcegroup}/providers/Microsoft.Resources/deployments/?$filter=provisioningState eq 'Failed'&$top=5&api-version=2018-02-01",
                    "jTokenPath": "value",
                    "textProperty": "id",
                    "valueProperty": "id",
                    "textPropertyRegex": "[^/]+$"
                    },
                    "dropdownOptions": [{
                      "value": "Unable to get the list of operation failures or no exist for this resource group.",
                      "text": "Unable to get the list of operation failures or no exist for this resource group.",
                    }
                    ],
                    "required": false
                }
                ]
}
---
