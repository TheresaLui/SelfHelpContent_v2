<properties
	pageTitle="Point-to-site client side issues"
	description="Point-to-site client side issues"
	authors="radwiv"
 	ms.author="radwiv"
	selfHelpType="problemScopingQuestions"
	articleid="vpngwp2sclientsideissues"
	supportTopicIds="32633158"
	productPesIds="16094"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="CloudNet_AzureVPNGateway"
/>
# Point-to-site client side issues
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Point-to-site client side issues",
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
                    "text": "Other"
                }
            ],
            "required": true
        },
        {
            "id": "Issue_type",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Select the issue type",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Download",
                    "text": "Problem in generating or downloading profile"
                },
                {
                    "value": "Installation",
                    "text": "Problem in profile installation"
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
