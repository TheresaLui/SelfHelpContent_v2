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
                "title": "My desired region or VM size is unavailable",
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
                },
                {
                  "id": "selectregion",                  
                  "order": 2,                  
                  "controlType": "dropdown",                  
                  "displayLabel": "What is the region you are deploying in?",                  
                  "watermarkText": "Choose an option",                  
                  "dropdownOptions": [{                    
                    "value": "It's slower that it typically is",
                    "text": "It's slower that it typically is"                    
                    }, {
                      "value": "Another virtual machine in the subscription is faster",                      
                      "text": "Another virtual machine in the subscription is faster"                      
                      }, {
                        "value": "Benchmarking tests not meeting minimum Azure specifications",
                        "text": "Benchmarking tests not meeting minimum Azure specifications"
                        }, {

                          "value": "It's faster in a non-Azure environment",

                          "text": "It's faster in a non-Azure environment"

                        }

                        ],

                        "required": false
                      }

                {
                  "id": "deployment_size",
                  "order": 3,
                  "controlType": "multilinetextbox",
                  "displayLabel": "What is the size of the VM you are trying to deploy?",
                  "required": false,
                  "useAsAdditionalDetails": true,
                  "hints": [{
                    "text": "Size of the virtual machine you are trying to deploy."
                    }]
                  },{
                    "id": "deployment_isinavailabilityset",
                    "order": 4,
                    "controlType": "dropdown",
                    "displayLabel": "Are you deploying your VM in an availability set?",
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
