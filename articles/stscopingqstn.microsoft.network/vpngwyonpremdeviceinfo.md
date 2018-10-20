<properties
	pageTitle="Provide On Prem Device"
	description="Provide On Prem Device"
	authors="KristinaNeyens"
	selfHelpType="problemScopingQuestions"
	articleid="ProvideOnPremDevice"
	supportTopicIds="32591152, 32591149, 32591158"
	productPesIds="16094"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# VPN Gwy On Prem Device
---
{
	"resourceRequired": false,
	"title": "VPN Gwy On Prem Device",
	"fileAttachmentHint": "Upload your VPN configuration file. Make sure you edit or remove any pre-shared keys or secrets from the file",
	"formElements": [{
			"id": "Provide VPN On Premise device",
			"order": 1,
			"controlType": "dropdown",
			"displayLabel": "Choose the device you are using",
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
			"id": "When did the problem start?",
			"order": 2,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true
		}, {
			"id": "Additional details",
			"order": 5,
			"controlType": "multilinetextbox",
			"displayLabel": "Please provide device Model and iOS/firmware version",
			"required": false,
			"useAsAdditionalDetails": true,
			"hints": [
                {
                    "text": "Issue description"
                },
                {
                    "text": "Make, model and OS version of on-premises VPN device(s) (for example, \"Cisco ASA 5505 OS version 8.3\")"
                },
                {
                    "text": "Upload your configuration file to speed the support process"
                },
                {
                    "text": "For security purposes, please edit or remove the pre-shared key field from the configuration information"
                }
            ]
		}, {
			"id": "learn_more_text",
			"order": 6,
			"controlType": "infoblock",
			"content": "<a href='https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-deviceshttps://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-devices?toc=%2Fazure%2Fvpn-gateway%2F%2Ftoc.json'>Learn more</a> about Validated VPN Devices and our device configuration guides"
		}
	]
}
---
