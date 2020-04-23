<properties
	articleId="problemscopingques-netappvolume-connectivity"
	pageTitle="Unable connect to a NetApp volume"
	description="NetApp volumes connectivity scoping questions"
	authors="ram-kakani"
	ms.author="ramakk"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32640618"
	productPesIds="16469"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureNetAppFiles"
/>
# NetApp volume connectivity issue
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Unable to connect to a NetApp volume",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "topology",
            "visibility": "null",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Where is the source machine located?",
            "watermarkText": "Choose a topology",
            "dropdownOptions": [
                {
                    "value": "In the same VNET",
                    "text": "In the same VNET"
                },
                {
                    "value": "In a peered VNET(same region)",
                    "text": "In a peered VNET(same region)"
                },
                {
                    "value": "On-premise, connected to this VNET with ExpressRoute",
                    "text": "On-premise, connected to this VNET with ExpressRoute"
                },
                {
                    "value": "On-premise, connected to this VNET with VPN Gateway",
                    "text": "On-premise, connected to this VNET with VPN Gateway"
                },
                {
                    "value": "On-premise, connecting over ExpressRoute and VNET peering",
                    "text": "On-premise, connecting over ExpressRoute and VNET peering"
                },
                {
                    "value": "On-premise, connecting over VPN Gateway and VNET peering",
                    "text": "On-premise, connecting over VPN Gateway and VNET peering"
                },
                {
                    "text": "Other or none of the above",
                    "value": "dont_know_answer"
                }
            ],
            "required": true
        },
        {
            "id": "resourceGroup",
            "order": 4,
            "visibility": "topology == In the same VNET || topology == In a peered VNET(same region)",
            "controlType": "dropdown",
            "displayLabel": "Provide the Resource Group name of the source VM",
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
            "id": "VMName",
            "order": 5,
            "visibility": "resourceGroup != null",
            "controlType": "dropdown",
            "displayLabel": "Provide the name of the source VM",
            "watermarkText": "Filter by name",
            "dynamicDropdownOptions": {
                "dependsOn": "resourceGroup",
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
            "DropdownOptions": [
                {
                    "value": "Unable to retrieve list of VMs",
                    "text": "Unable to retrieve list of VMs"
                }
            ],
            "required": true
        },
        {
            "id": "HubVNET",
            "order": 6,
            "visibility": "topology == On-premise, connected to this VNET with ExpressRoute || topology == On-premise, connected to this VNET with VPN Gateway || topology == On-premise, connecting over ExpressRoute and VNET peering || topology==On-premise, connecting over VPN Gateway and VNET peering",
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
            "DropdownOptions": [
                {
                    "value": "Unable to retrieve list of VNETs",
                    "text": "Unable to retrieve list of VNETs"
                }
            ],
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 100,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
