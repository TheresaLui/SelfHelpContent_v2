<properties
	pageTitle="Azure Information Client - Can't apply this label error"
	description="Azure Information Client - Can't apply this label error"
	authors="orbarak-ms"
	ms.author="orbarak"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32584334"
    productPesIds="14997"
    cloudEnvironments="Public"
    articleId="scoping_cant_apply_label"
	schemaVersion="1"
/>
# Can't apply this label
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "Can't apply this label",
				"subscriptionRequired": "false",
                "fileAttachmentHint": "Export AIP logs Using Protect/Sensitivity -> Help and Feedback -> Export Logs",
                "formElements": [
                {
                "id": "cant_apply_label",
                "order": 1,
                "controlType": "multilinetextbox",
                "displayLabel": "What is the error you received?",
                "required": false,
                "useAsAdditionalDetails": true
                },{
                    "id": "client_type",
                    "order": 2,
                    "controlType": "dropdown",
                    "displayLabel": "Which AIP client are you using?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                        {
                            "value": "Azure Information Protection Classic Client",
                            "text": "Azure Information Protection Classic Client"
                        },
                        {
                            "value": "Azure Information Protection Unified Labeling Client",
                            "text": "Azure Information Protection Unified Labeling Client"
                        },
	                    {
							"value": "dont_know_answer",
							"text": "I don't know"
						}
                    ],
                    "required": true
                },{
                "id": "version_number_classic",
                "order": 3,
                "visibility": "client_type == Azure Information Protection Classic Client",
                "controlType": "dropdown",
                "displayLabel": "What version are you using? if it's not listed, please upgrade",
                "watermarkText": "Choose an option",
                "dropdownOptions": [
                    {
                        "value": "1.53.10.0",
                        "text": "1.53.10.0"
                    },
                    {
                        "value": "1.48.204.0",
                        "text": "1.48.204.0"
                    },
                    {
                        "value": "1.41.51.0",
                        "text": "1.41.51.0"
                    },
                    {
						"value": "dont_know_answer",
						"text": "I don't know"
                    }
                ],
                "required": true
                },{
                "id": "version_number_ul",
                "order": 4,
                "visibility": "client_type == Azure Information Protection Unified Labeling Client",
                "controlType": "dropdown",
                "displayLabel": "What version are you using? if it's not listed, please upgrade",
                "watermarkText": "Choose an option",
                "dropdownOptions": [
                    {
                        "value": "2.2.19.0",
                        "text": "2.2.19.0"
                    },
                    {
                        "value": "2.2.14.0",
                        "text": "2.2.14.0"
                    },
                    {
                        "value": "2.0.779.0",
                        "text": "2.0.779.0"
                    },
                    {
                        "value": "2.0.778.0",
                        "text": "2.0.778.0"
                    },
                    {
						"value": "dont_know_answer",
						"text": "I don't know"
                    }
                ],
                "required": true
                },{
                    "id": "sccmigrate
                    "order": 5
                    "visibility": "client_type == Azure Information Protection Classic Client",
                    "controlType": "dropdown",
                    "displayLabel": "Did you activate Unified Labeling in your tenant?",
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
                },{
                    "id": "ipprivate",
                    "order": 7,
                    "visibility": "ippublicprivate == Private IP",
                    "controlType": "dropdown",
                    "displayLabel": "Are you able to connect to the Public IP?",
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
                            "value": "I don't have a Public IP",
                            "text": "I don't have a Public IP"
                        }
                    ],
                    "required": false
                },{
                    "id": "connect_subnet",
                    "order": 8,
                    "visibility": "ippublic == No || ipprivate == No || ipprivate == I don't have a Public IP",
                    "controlType": "dropdown",
                    "displayLabel": "Is the problem isolated when you are connecting from a specific subnet?",
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
                },{
                    "id": "connect_ifnew",
                    "order": 9,
                    "controlType": "dropdown",
                    "displayLabel": "Is this VM new to Azure?",
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
                    "id": "connect_from",
                    "order": 10,
                    "visibility": "connect_ifnew == Yes",
                    "controlType": "dropdown",
                    "displayLabel": "Where is the VM from?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                        {
                            "value": "On premise",
                            "text": "On premise"
                        },
                        {
                            "value": "From ASM to ARM",
                            "text": "From ASM to ARM"
                        },
                        {
                            "value": "From another cloud provider",
                            "text": "From another cloud provider"
                        }
                    ],
                    "required": false
                },{
                    "id": "connect_howmigrated",
                    "order": 11,
                    "visibility": "connect_from == On premise || connect_from == From another cloud provider",
                    "controlType": "dropdown",
                    "displayLabel": "How was this machine migrated?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                        {
                            "value": "I used Azure Site Recovery",
                            "text": "I used Azure Site Recovery"
                        },
                        {
                            "value": "I used a third-party migration tool",
                            "text": "I used a third-party migration tool"
                        },
                        {
                            "value": "I uploaded the disk manually",
                            "text": "I uploaded the disk manually"
                        },
                        {
                            "value": "I used Azure Migrate",
                            "text": "I used Azure Migrate"
                        }
                    ],
                    "required": false
                },{
                    "id": "connect_wasoncloud",
                    "order": 12,
                    "visibility": "connect_from == On premise",
                    "controlType": "dropdown",
                    "displayLabel": "Was the machine prepared to work on a cloud environment prior the migration?",
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
                },{
                      "id": "connect_ifbackup",
                      "order": 13,
                      "controlType": "dropdown",
                      "displayLabel": "Was this VM recovered from backup?",
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
                      "id": "connect_ifinternet",
                      "order": 14,
                      "controlType": "dropdown",
                      "displayLabel": "Do you have connectivity issues from/to this VM?",
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
                  },{
                      "id": "connect_internetissue",
                      "order": 15,
                      "visibility": "connect_ifinternet == Yes",
                      "controlType": "dropdown",
                      "displayLabel": "What is the problem you are having?",
                      "watermarkText": "Choose an option",
                      "dropdownOptions": [
                          {
                              "value": "Cannot connect to the RDP port",
                              "text": "Cannot connect to the RDP port"
                          },
                          {
                              "value": "Cannot connect to the Powershell port",
                              "text": "Cannot connect to the Powershell port"
                          },
                          {
                              "value": "Cannot connect to my SQL instance",
                              "text": "Cannot connect to my SQL instance"
                          },
                          {
                              "value": "Cannot connect to another port",
                              "text": "Cannot connect to another port"
                          },
                          {
                              "value": "My VM doesn't have access to Internet",
                              "text": "My VM doesn't have access to Internet"
                          }
                      ],
                      "required": false
                  },{
                    "id": "problem_description",
                    "order": 16,
                    "controlType": "multilinetextbox",
                    "displayLabel": "Description",
                    "useAsAdditionalDetails": false,
                    "required": true
                    },{
                    "id": "problem_start_time",
                    "order": 17,
                    "controlType": "datetimepicker",
                    "displayLabel": "When did the problem start?",
                    "required": true
                  }
                  ]
}
---
