{
                "resourceRequired": true,
                "title": "I received a provisioning or deployment timeout error",
                "fileAttachmentHint": "",
                "formElements": [{
                                        "id": "selectfailedoperation",
                                        "order": 1,
                                        "controlType": "dropdown",
                                        "displayLabel": "Please select the Operation name you are experiencing a deployment failure with",
                                        "watermarkText": "Choose an option",
                                        "dynamicDropdownOptions": {
                                                  uri": "/subscriptions/{subscriptionid}/resourceGroups/{resourcegroup}/providers/Microsoft.Resources/deployments/?$filter=provisioningState eq 'Failed'&$top=5&api-version=2018-02-01",
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
                                },{
                                  			"id": "deployment_imagetype",
                                  			"order": 1,
                                  			"controlType": "dropdown",
                                  			"displayLabel": "Choose the type of image deployment",
                                  			"watermarkText": "Choose an option",
                                  			"dropdownOptions": [{
                                  					"value": "Custom Image",
                                  					"text": "Custom Image"
                                  				},{
                                  					"value": "Marketplace Image",
                                  					"text": "Marketplace Image"
                                  				},{
                                  					"value": "I do not know",
                                  					"text": "I do not know"
                                  				}
                                  				],
                                  			"required": false
                                		},{
                                      			"id": "deployment_isrunning",
                                      			"order": 1,
                                      			"controlType": "dropdown",
                                      			"displayLabel": "Is your image started and running?",
                                      			"watermarkText": "Choose an option",
                                      			"dropdownOptions": [{
                                      					"value": "Is started running",
                                      					"text": "Is started running"
                                      				},{
                                      					"value": "Is not started",
                                      					"text": "Is not started"
                                      				},{
                                      					"value": "I do not know",
                                      					"text": "I do not know"
                                      				}
                                      				],
                                      			"required": false
                                    		}
                                  ]
}
