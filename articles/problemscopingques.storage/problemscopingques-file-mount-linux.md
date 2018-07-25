<properties
	pageTitle="Storage File Share mounting issues - Linux"
	description="Storage File Share mounting issues - Linux"
	authors="Passaree"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32602763"
	productPesIds="16460"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Storage File Share mounting issues - Linux
---
{
	"resourceRequired": true,
	"title": "Storage File Share mounting issues - Linux",
	"fileAttachmentHint": "",
	"formElements": [{
			"id": "mount_location",
			"order": 1,
			"controlType": "dropdown",
			"displayLabel": "Location where File Share is being mounted",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "same_region",
					"text": "Azure VM is in same region as the Azure File Share"
				}, {
					"value": "different_region",
					"text": "Azure VM is in different region than the Azure File Share"
				}, {
					"value": "on_premises",
					"text": "Client is outside Azure"
				}
			],
			"required": true
		}, {
			"id": "os_version",
			"order": 2,
			"controlType": "dropdown",
			"displayLabel": "Linux version where File Share is being mounted",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Ubuntu_below1404",
					"text": "Ubuntu Server below 14.04"
				}, {
					"value": "Ubuntu_1404_1510",
					"text": "Ubuntu Server 14.04 - 15.10"
				}, {
					"value": "Ubuntu_above1604",
					"text": "Ubuntu Server 16.04 or above"
				}, {
					"value": "rhel_below7",
					"text": "RHEL below 7"
				}, {
					"value": "rhel_7_74",
					"text": "RHEL 7.0 - 7.4"
				}, {
					"value": "rhel_above75",
					"text": "RHEL 7.5 or above"
				}, {
					"value": "CentOS_below7",
					"text": "CentOS below 7"
				}, {
					"value": "CentOS_7_74",
					"text": "CentOS 7.0 - 7.4"
				}, {
					"value": "CentOS_above75",
					"text": "CentOS 7.5 or above"
				}, {
					"value": "Debian_below8",
					"text": "Debian below 8"
				}, {
					"value": "Debian_above8",
					"text": "Debian 8 or above"
				}, {
					"value": "OpenSUSE_below132",
					"text": "OpenSUSE below 13.2"
				}, {
					"value": "OpenSUSE_132_422",
					"text": "OpenSUSE 13.2 - 42.2"
				}, {
					"value": "OpenSUSE_above423",
					"text": "OpenSUSE 42.3 or above"
				}, {
					"value": "other",
					"text": "Other - provide Linux kernel version below"
				}
			],
			"required": true
		}, {
			"id": "linux_kernel",
			"order": 3,
			"controlType": "textbox",
			"displayLabel": "Linux kernel version",
			"watermarkText": "Run 'uname -r' command to find Linux kernel version",
			"required": false
		}, {
			"id": "additional_details",
			"order": 4,
			"controlType": "multilinetextbox",
			"displayLabel": "Provide any additional details",
			"required": false,
			"useAsAdditionalDetails": true
		}
	]
}
---
