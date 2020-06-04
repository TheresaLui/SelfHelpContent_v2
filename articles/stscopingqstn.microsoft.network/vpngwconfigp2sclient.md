<properties
	pageTitle="Configure a point-to-site client information"
	description="Configure a point-to-site client information"
	authors="radwiv"
 	ms.author="radwiv"
	selfHelpType="problemScopingQuestions"
	articleid="vpngwconfigp2sclient"
	supportTopicIds="32633156"
	productPesIds="16094"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="CloudNet_AzureVPNGateway"
/>
# Configure a point-to-site client information
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Configure a point-to-site client",
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
            "id": "problem_description",
            "order": 4,
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
