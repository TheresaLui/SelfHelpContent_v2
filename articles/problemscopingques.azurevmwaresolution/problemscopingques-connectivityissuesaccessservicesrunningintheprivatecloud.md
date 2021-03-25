<properties
	articleId="accessservicesrunninginprivatecloud"
	pageTitle="accessservicesrunninginprivatecloud"
	description="AVS connectivity - access scoping questions"
	authors="neshenoy"
	ms.author="neshenoy"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32743018"
	productPesIds="17080"
	cloudEnvironments="Public,FairFax, usnat, ussec"
	schemaVersion="1"
	ownershipId="Azure_VMwareSolution_Content"
/>
# connectivity issue Access services running in the private cloud 
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Access services running in the private cloud",
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
                    "value": "In a peered VNET (same region)",
                    "text": "In a peered VNET (same region)"
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
            "order": 2,
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
            "order": 3,
            "visibility": "resourceGroup != null",
            "controlType": "dropdown",
            "displayLabel": "Provide the name of the source VM",
            "watermarkText": "Filter by name",
            "dynamicDropdownOptions": {
                "dependsOn": "resourceGroup",
                "uri": "/subscriptions/{subscriptionId}/providers/Microsoft.Compute/virtualMachines?api-version=2020-06-01",
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
            "order": 4,
            "visibility": "topology == On-premise, connected to this VNET with ExpressRoute || topology == On-premise, connected to this VNET with VPN Gateway || topology == On-premise, connecting over ExpressRoute and VNET peering || topology==On-premise, connecting over VPN Gateway and VNET peering",
            "controlType": "dropdown",
            "displayLabel": "Choose the virtual network connected to your on-premise network",
            "watermarkText": "Choose a virtual network",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionId}/providers/Microsoft.Network/virtualWans?api-version=2020-07-01",
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
            "id": "ipaddress",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "What is the IP address you're having trouble connecting to?",
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 100,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": false
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
