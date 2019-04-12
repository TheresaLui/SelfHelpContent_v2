<properties
	articleId="problemscopingques-netappvolume-connectivity"
	pageTitle="Unable connect to a NetApp volume"
	description="NetApp volumes connectivity scoping questions"
	authors="ram-kakani"
	ms.author="ramakk"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32606353"
	productPesIds="16469"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# NetApp volume connectivity issue
---
{
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
            "dropdownOptions": [{
                    "value": "In the same VNET",
                    "text": "In the same VNET"
                }, {
                    "value": "In a peered VNET(same region)",
                    "text": "In a peered VNET(same region)"
                }, {
                    "value": "On-premise, connected to this VNET with virtual network gateway",
                    "text": "On-premise, connected to this VNET with virtual network gateway"
                }, {
										"value": "On-premise, connected to this VNET via a Hub VNET",
										"text": "On-premise, connected to this VNET via a Hub VNET"
								}
              ],
            "required": true
				}, {
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
            "textPropertyRegex": "[^/]+$"
						},
						"defaultDropdownOptions": [{
                    "value": "Unable to get the Resource Group",
                    "text": "Unable to get the Resource Group"
                }
            ],
            "required": true
				}, {
					"id": "VMName",
            "order": 5,
            "visibility": "resourceGroup != null",
            "controlType": "dropdown",
            "displayLabel": "Provide the name of the source VM",
            "watermarkText": "Filter by name",
						"dynamicDropdownOptions": {
						"dependsOn":"resourceGroup",
						"uri": "/subscriptions/{subscriptionId}/resourceGroups/{replaceWithParentValue}/providers/Microsoft.Compute/virtualMachines?api-version=2018-06-01",
            "jTokenPath": "value",
            "textProperty": "name",
            "valueProperty": "id",
            "textPropertyRegex": "[^/]+$"
						},
						"defaultDropdownOptions": [{
                    "value": "Unable to get the VM",
                    "text": "Unable to get the VM"
                }
            ],
            "required": true
				}, {
					"id": "GatewayType",
            "order": 6,
            "visibility": "topology == On-premise, connected to this VNET with virtual network gateway || topology == On-premise, connected to this VNET via a Hub VNET",
            "controlType": "dropdown",
            "displayLabel": "Chose the virtual network gateway type",
            "watermarkText": "Choose a gateway type",
						"dropdownOptions": [{
                    "value": "VPN gateway",
                    "text": "VPN gateway"
                }, {
                    "value": "ExpressRoute gateway",
                    "text": "ExpressRoute gateway"
                }
              ],
            "required": true
				}, {
					"id": "HubVNET",
            "order": 7,
            "visibility": "topology == On-premise, connected to this VNET with virtual network gateway || topology == On-premise, connected to this VNET via a Hub VNET",
            "controlType": "dropdown",
            "displayLabel": "Chose the virtual network connected to on-premise",
						"watermarkText": "Choose a virtual network",
						"dynamicDropdownOptions": {
            "uri": "/subscriptions/{subscriptionId}/providers/Microsoft.Network/virtualNetworks?api-version=2018-11-01",
            "jTokenPath": "value",
            "textProperty": "name",
            "valueProperty": "id",
            "textPropertyRegex": "[^/]+$"
						},
						"dropdownOptions": [{
                    "value": "Unable to get the virtual network",
                    "text": "Unable to get the virtual network"
              }
            ],
            "required": true
				}, {
            "id": "problem_start_time",
            "order": 100,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }, {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ]
}
---
