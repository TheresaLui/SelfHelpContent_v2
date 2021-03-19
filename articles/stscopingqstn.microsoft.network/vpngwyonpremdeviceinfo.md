<properties
	pageTitle="Provide On Prem Device"
	description="Provide On Prem Device"
	authors="radwiv"
	ms.author="radwiv"
	selfHelpType="problemScopingQuestions"
	articleid="ProvideOnPremDevice"
	supportTopicIds="32591149, 32591152, 32633157, 32584874"
	productPesIds="16094,15526"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="CloudNet_AzureVPNGateway"
/>
# VPN Gwy On Prem Device
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "VPN Gwy On Prem Device",
    "fileAttachmentHint": "Upload your VPN configuration file. Make sure you edit or remove any pre-shared keys or secrets from the file",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "Provide VPN On Prem device",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Select the device you are using",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "A10 Networks",
                    "text": "A10 Networks"
                },
                {
                    "value": "Allied Telesis",
                    "text": "Allied Telesis"
                },
                {
                    "value": "Barracuda Networks, Inc.",
                    "text": "Barracuda Networks, Inc."
                },
                {
                    "value": "Brocade",
                    "text": "Brocade"
                },
                {
                    "value": "Check Point",
                    "text": "Check Point"
                },
                {
                    "value": "Cisco ASA",
                    "text": "Cisco ASA"
                },
                {
                    "value": "Cisco ASR",
                    "text": "Cisco ASR"
                },
                {
                    "value": "Cisco ISR",
                    "text": "Cisco ISR"
                },
                {
                    "value": "Cisco Meraki",
                    "text": "Cisco Meraki"
                },
                {
                    "value": "Citrix",
                    "text": "Citrix"
                },
                {
                    "value": "F5",
                    "text": "F5"
                },
                {
                    "value": "Fortinet",
                    "text": "Fortinet"
                },
                {
                    "value": "Internet Initiative Japan",
                    "text": "Internet Initiative Japan"
                },
                {
                    "value": "Juniper",
                    "text": "Juniper"
                },
                {
                    "value": "Microsoft",
                    "text": "Microsoft"
                },
                {
                    "value": "Open Systems AG",
                    "text": "Open Systems AG"
                },
                {
                    "value": "Palo Alto Networks",
                    "text": "Palo Alto Networks"
                },
                {
                    "value": "ShareTech",
                    "text": "ShareTech"
                },
                {
                    "value": "SonicWall",
                    "text": "SonicWall"
                },
                {
                    "value": "Sophos",
                    "text": "Sophos"
                },
                {
                    "value": "Ubiquiti",
                    "text": "Ubiquiti"
                },
                {
                    "value": "WatchGuard",
                    "text": "WatchGuard"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other"
                }
            ],
            "required": true
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide device model and iOS/firmware version",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Issue description"
                },
                {
                    "text": "Make, model and OS version of on-premises VPN device(s) (for example, \"Cisco ASA 5505 OS version 8.3\")"
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---
