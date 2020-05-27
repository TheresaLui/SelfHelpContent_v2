<properties
    pageTitle="Unable to connect to a SAP Hana instance"
    description="Problem scoping for SAP HANA on Azure Large Instance Connectivity"
    authors="tizape"
    ms.author="tizape"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32632357,32632371,32632369,32632372,32632367,32632342"
    productPesIds="16208,15571,15797"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="80aa8522-57d5-4826-ac41-51e412abf20d"
	ownershipId="Compute_AppService"
/>


# Unable to connect to a SAP Hana instance
---
{
	"subscriptionRequired": true,
	"resourceRequired": true,
	"title": "Unable to connect to a SAP Hana instance",
	"fileAttachmentHint": "",
	"formElements": [{
			"id": "topology",
			"order": 1,
            "visibility": null,
			"controlType": "dropdown",
			"displayLabel": "Where is the source traffic coming from?",
			"watermarkText": "Choose a topology",
			"dropdownOptions": [
                {
					"value": "On Premise to HANA",
					"text": "On Premise to HANA"
				},
				{
					"value": "Azure to HANA (same Region)",
					"text": "Azure to HANA (same Region)"
				},
				{
					"value": "Azure to HANA (across Region)",
					"text": "Azure to HANA (across Region)"
				},
				{
					"text": "Other or none of the above",
					"value": "dont_know_answer"
				}
			],
			"required": true
		},
		{
			"id": "sourceVMresourceGroup",
			"order": 2,
			"visibility": "topology == Azure to HANA (same Region) || topology == Azure to HANA (across Region)",
			"controlType": "dropdown",
			"displayLabel": "Please provide the Resource Group name of the Source VM",
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
			"DropdownOptions": [{
				"value": "Unable to retrieve list of resource groups",
				"text": "Unable to retrieve list of resource groups"
			}],
			"required": true
		},
		{
			"id": "sourceVMName",
			"order": 3,
			"visibility": "topology != On Premise to HANA && sourceVMresourceGroup != null",
			"controlType": "dropdown",
			"displayLabel": "Provide the Name of the source VM",
			"watermarkText": "Filter by name",
			"dynamicDropdownOptions": {
				"dependsOn": "sourceVMresourceGroup",
				"uri": "/subscriptions/{subscriptionId}/resourceGroups/{replaceWithParentValue}/providers/Microsoft.Compute/virtualMachines?api-version=2018-06-01",
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
			"DropdownOptions": [{
				"value": "Unable to retrieve list of VMs",
				"text": "Unable to retrieve list of VMs"
			}],
			"required": true
		},
		{
			"id": "HubVNET",
			"order": 4,
			"visibility": "topology == On Premise to HANA",
			"controlType": "dropdown",
			"displayLabel": "Chose the virtual network connected to your on-premise network",
			"watermarkText": "Choose a virtual network",
			"dynamicDropdownOptions": {
				"uri": "/subscriptions/{subscriptionId}/providers/Microsoft.Network/virtualNetworks?api-version=2018-11-01",
				"jTokenPath": "value",
				"textProperty": "name",
				"valueProperty": "id",
				"textPropertyRegex": "[^/]+$",
				"defaultDropdownOptions": {
					"value": "dont_know_answer",
					"text": "Other or none of the above"
				}
			},
			"DropdownOptions": [{
				"value": "Unable to retrieve list of VNETs",
				"text": "Unable to retrieve list of VNETs"
			}],
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
			"hints": [{
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
