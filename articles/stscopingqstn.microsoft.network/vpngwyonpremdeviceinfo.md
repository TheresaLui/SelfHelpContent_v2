<properties
	pageTitle="Provide On Prem Device"
	description="Provide On Prem Device"
	authors="KristinaNeyens"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32591152, 32591149, 32591158,"
	productPesIds="16094"
	cloudEnvironments=""
	schemaVersion="1"
/>
# VPN Gwy On Prem Device
---
{
	"resourceRequired": false,
	"title": "VPN Gwy On Prem Device",
	"fileAttachmentHint": "",
	"formElements": [{
			"id": "Provide VPN On Premise Device",
			"order": 1,
			"controlType": "dropdown",
			"displayLabel": "Please provide VPN On Premise Device you are using",
			"watermarkText": "Choose a device",
			"dropdownOptions": [{
					"value": "A10 Networks",
					"text": "A10 Networks"
				}, {
					"value": "Allied Telesis",
					"text": "Allied Telesis"
				}, {
					"value": "Barracuda Networks, Inc.",
					"text": "Barracuda Networks, Inc."
				}, {
					"value": "Brocade",
					"text": "Brocade"
				}, {
					"value": "Check Point",
					"text": "Check Point"
				}, {
					"value": "Cisco ASA",
					"text": "Cisco ASA"
				}, {
					"value": "Cisco ASR",
					"text": "Cisco ASR"
				}, {
					"value": "Cisco ISR",
					"text": "Cisco ISR"
				}, {
					"value": "Cisco Meraki - Not Compatible",
					"text": "Cisco Meraki - Not Compatible"
				}, {
					"value": "Citrix",
					"text": "Citrix"
				}, {
					"value": "F5",
					"text": "F5"
				}, {
					"value": "Fortinet",
					"text": "Fortinet"
				}, {
					"value": "Internet Initiative Japan",
					"text": "Internet Initiative Japan"
				}, {
					"value": "Juniper",
					"text": "Juniper"
				}, {
					"value": "Microsoft",
					"text": "Microsoft"
				}, {
					"value": "Open Systems AG",
					"text": "Open Systems AG"
				}, {
					"value": "Palo Alto Networks",
					"text": "Palo Alto Networks"
				}, {
					"value": "ShareTech",
					"text": "ShareTech"
				}, {
					"value": "SonicWall",
					"text": "SonicWall"
				}, {
					"value": "Sophos",
					"text": "Sophos"
				}, {
					"value": "Ubiquiti",
					"text": "Ubiquiti"
				}, {
					"value": "WatchGuard",
					"text": "WatchGuard"
				}, {
					"value": "Other - Please Specify",
					"text": "Other - Please Specify"

				}

			],
			"required": true
		}, {
			"id": "problem_start_date",
			"order": 2,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true
		
		}, {
			"id": "additional_details",
			"order": 5,
			"controlType": "multilinetextbox",
			"displayLabel": "Please provide device Model and iOS/firmware version",
			"required": false,
			"useAsAdditionalDetails": true,
			"hints": [{
					"text": "Example: Cisco ASA 5525 V.9.3"
				}, {
					"text": "Upload your configuration file to speed the support process; please edit or remove any pre-shared keys or secrets from the configuration information"
				}
			]
		}, {
			"id": "learn_more_text",
			"order": 6,
			"controlType": "infoblock",
			"content": "<a href='https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpn-devices>Learn more</a> about Validated VPN Devices and our device configuration guides"
		}
	]
}
---
