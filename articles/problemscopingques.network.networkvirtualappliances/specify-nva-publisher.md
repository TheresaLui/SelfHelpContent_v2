<properties
	pageTitle="NVA in the Virtual WAN Hub Publisher"
	description="Scoping questions to capture more details about errors encountered while connecting to SQL DB"
	ms.author="scottnap"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32743826,32743827,32743819,32743820,32743821,32743822,32743823,32743824,32743825"
	productPesIds="16572"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="a522beba-5a48-4e1e-be06-f905b9dd1708"
	ownershipId="CloudNet_VirtualWAN"
/>
# Please specify the NVA Publisher
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Specify NVA Publisher",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "Specify the Publisher of the NVA",
        "description": "Please specify the Publisher of the Network Virtual Appliance you're experiencing issues with.",
        "insightNotAvailableText": "Insight Not Available."
    },
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "infoBalloonText": "Enter the approximate time you started to see the error.",
            "required": true,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "publisher_dropdown",
            "order": 10,
            "controlType": "dropdown",
            "displayLabel": "Please specify the Publisher of the NVA in the Virtual WAN Hub you're having trouble with.",
            "watermarkText": "Choose an option",
            "infoBalloonText": "Select NVA Publisher (e.g. Barracuda)",
            "dropdownOptions": [
                {
                    "value": "barracuda",
                    "text": "Barracuda Networks"
                },
                {
                    "value": "dont_know_answer",
                    "text": "I'm not sure"
                }
            ],
            "required": true,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional context for the issue you are encountering.",
            "required": true,
            "useAsAdditionalDetails": true,
            "watermarkText": "Please give us as many details as you can about the problem you're having."
        }

    ]
}
---
