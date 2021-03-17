<properties
	articleid="vpngwpointtositeconn"
	pageTitle="Point-to-Site VPN connectivity issues information"
	description="Point-to-Site VPN connectivity issues information"
	authors="radwiv"
        ms.author="radwiv"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32591156,32584878"
	productPesIds="16094,15526"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="CloudNet_AzureVPNGateway"
/>
# Point-to-Site VPN connectivity issues information
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Point-to-site connectivity issues",
    "fileAttachmentHint": "Upload your VPN profile to speed up the support process. For security purposes, please edit or remove the client certificate information.",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "P2S_connectivity_issues",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Select the issue you're facing",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Connectionnotestablishing",
                    "text": "Connection not establishing or disconnecting frequently"
                },
                {
                    "value": "Notreachingdestination",
                    "text": "Not able to reach specific destination"
                },
                {
                    "value": "Packet drops",
                    "text": "Packet drops"
                },
                {
                    "value": "Throughput",
                    "text": "Throughput"
                },
                {
                    "value": "Latency",
                    "text": "Latency"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "source_dest_IP_address",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Provide source and destination IP addresses (on-premises and/ or VNet IP addresses)",
            "required": false,
            "useAsAdditionalDetails": false
        },
        {
            "id": "P2S_clientOS",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Select the Point-to-Site client OS",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Windows",
                    "text": "Windows"
                },
                {
                    "value": "iOS",
                    "text": "iOS"
                },
                {
                    "value": "Linux",
                    "text": "Linux"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
	 {
            "id": "OS_version",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "Enter Point-to-Site client OS version",
            "required": false,
            "useAsAdditionalDetails": false
        },
	{
            "id": "P2S_tunneltype",
            "order": 6,
            "controlType": "dropdown",
            "displayLabel": "Select the tunnel type",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "IKEv2",
                    "text": "IKEv2"
                },
                {
                    "value": "OpenVPN",
                    "text": "OpenVPN"
                },
                {
                    "value": "SSTP",
                    "text": "SSTP"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "P2S_authentication",
            "order": 7,
            "controlType": "dropdown",
            "displayLabel": "Select the authentication type",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Azure Active Directory",
                    "text": "Azure Active Directory"
                },
                {
                    "value": "RADIUS",
                    "text": "RADIUS"
                },
                {
                    "value": "Certificate",
                    "text": "Certificate"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": false
        },
        {
            "id": "P2S_custompolicy",
            "order": 8,
            "controlType": "dropdown",
            "displayLabel": "Using custom policy?",
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
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 9,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional issue description",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
