<properties
    pageTitle="SAP HANA on Azure Large Instances"
    description="Problem scoping for SAP HANA on Azure Large Instances"
    authors="phgantik,timbasham"
    ms.author="tibasham"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32549255,32549257,32549256,32549258,32549259,32632347,32632349,32632350,32632360,32632373,32632374,32632342,32632345,32632357,32632361,32632365,32632369,32632371,32632372,32632337,32632338,32632339,32632354,32632366,32632348,32632351,32632352,32632353,32632358,32632362,32632370,32632346,32632364,32632340,32632341,32632343,32632355,32632356,32632363,32632367,32632344,32632359,32632368"
    productPesIds="16208,15571,15797"
    cloudEnvironments="public"
    schemaVersion="1"
    articleId="3561f156-4abd-4450-9a71-792802e50f89"
/>


# SAP HANA on Azure Large Instances
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Configure SAP HANA large instances",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "configure_sap_hana",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Is this an Azure VM or a SAP HANA Large Instance",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Azure VM",
                    "text": "Azure VM(G-Series, M-Series,DS-Series etc)"
                },
                {
                    "value": "SAP HANA Large Instance",
                    "text": "SAP HANA Large Instance"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "resourceGroup",
            "order": 2,
            "visibility": "null",
            "controlType": "dropdown",
            "displayLabel": "Please provide the Resource Group name",
            "watermarkText": "Filter by name",
            "dynamicDropdownOptions": {
                    "uri": "/subscriptions/{subscriptionId}/resourcegroups?api-version=2018-05-01",
                    "jTokenPath": "value",
                    "textProperty": "name",
                    "valueProperty": "id",
                    "textPropertyRegex": "[^/]+$",
                    "defaultDropdownOptions": {
                        "value": "dont_know_answer",
                        "text": "Other or none of the above"
                    }
            },
            "DropdownOptions": [
                {
                    "value": "Unable to retrieve list of resource groups",
                    "text": "Unable to retrieve list of resource groups"
                }
            ],
            "required": true
        },
        {
            "id": "sapHanaBareMetalInstance",
            "order": 3,
            "visibility": "configure_sap_hana == SAP HANA Large Instance || resourceGroup != null",
            "controlType": "dropdown",
            "displayLabel": "Please select your SAP Hana Large Instance",
            "watermarkText": "Filter by name",
            "dynamicDropdownOptions": {
                "dependsOn": "resourceGroup",
                "uri": "/subscriptions/{subscriptionId}/resourceGroups/{replaceWithParentValue}/providers/Microsoft.HanaonAzure?api-version=2018-06-01",
                "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
		        "valuePropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Other or none of the above"
                }
            },
            "DropdownOptions": [
                {
                    "value": "Unable to retrieve list of SAP Hana Large Instances",
                    "text": "Unable to retrieve list of SAP Hana Large Instances"
                }
            ],
            "required": true
        },
        {
            "id": "sapHanaVMInstance",
            "order": 4,
            "visibility": "configure_sap_hana == Azure VM || resourceGroup != null",
            "controlType": "dropdown",
            "displayLabel": "Please select your SAP Hana VM Instance",
            "watermarkText": "Filter by name",
            "dynamicDropdownOptions": {
                "dependsOn": "resourceGroup",
                "uri": "/subscriptions/{subscriptionId}/resourceGroups/{replaceWithParentValue}/providers/Microsoft.Compute/virtualMachines?api-version=2018-06-01"
                "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
		        "valuePropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Other or none of the above"
                }
            },
            "DropdownOptions": [
                {
                    "value": "Unable to retrieve list of SAP Hana VMs",
                    "text": "Unable to retrieve list of SAP Hana VMs"
                }
            ],
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 100,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 200,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional details",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Names of the SAP HANA Instances."
                },
                {
                    "text": "The IP address of the SAP HANA Instance"
                },
                {
                    "text": "Note: Make sure you have selected the subscription which contains the SAP HANA Instance while creating this case"
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---
