<properties
   pageTitle="Scoping questions for VPN Gateway Issues"
   description="Scoping questions for VPN Gateway Issues"
   authors="radwiv"
   ms.author="radwiv"
   selfHelpType="problemScopingQuestions"
   supportTopicIds="32591150,32591151,32591159,32591155,32591154,32591157,32591153"
   productPesIds="16094"
   cloudEnvironments="public,fairfax,blackforest,moonCake, usnat, ussec"
   schemaVersion="1"
   articleId="e7d714bd-eb61-42d8-8270-df52d8514149"
	ownershipId="CloudNet_AzureVPNGateway"
/>
# VPN Gateway Issues
---
{
    "resourceRequired": false,
    "fileAttachmentHint": "Upload your VPN configuration file. Make sure you edit or remove any pre-shared keys or secrets from the file",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "Problem start time",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 2,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
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
