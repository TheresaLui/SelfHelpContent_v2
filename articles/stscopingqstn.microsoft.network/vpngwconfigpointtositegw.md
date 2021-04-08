<properties
	articleid="vpngwconfigpointtositegw"
	pageTitle="Configure Point-to-Site VPN Gateway"
	description="Configure Point-to-Site VPN Gateway"
	authors="radwiv"
        ms.author="radwiv"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32591148"
	productPesIds="16094"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="CloudNet_AzureVPNGateway"
/>
# Point-to-Site VPN Gateway Configuration information
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Point-to-site VPN Gateway Configuration information",
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
            "id": "tunnel_type",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Select the tunnel type",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "IKEv2",
                    "text": "IKEv2"
                },
                {
                    "value": "SSTP",
                    "text": "SSTP"
                },
                {
                    "value": "OpenVPN",
                    "text": "OpenVPN"
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
            "order": 3,
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
            "required": true
        },
        {
            "id": "P2S_custompolicy",
            "order": 4,
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
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Issue description"
                },
                {
                    "text": "Client platform OS version"
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---
