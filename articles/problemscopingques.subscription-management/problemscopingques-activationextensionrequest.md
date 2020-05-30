<properties
	pageTitle="Scoping questions for Activation Extension Request"
	description="Scoping questions for Activation Extension Request"
	authors="prdasneo"
	ms.author="prdasneo"
          selfHelpType="problemScopingQuestions"
	supportTopicIds="32632947"
	productPesIds="15660"
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
    schemaVersion="1"
   articleId="ActivationExtensionRequest-problemscopingquestion"
	ownershipId="ASMS_SubscriptionManagement"
/>
#  Activation Extension Request
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": " Activation Extension Request",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "Problem Start Date",
            "required": true
        },
        {
            "id": "SubscriptionId",
            "order": 9,
            "controlType": "dropdown",
            "displayLabel": "Select the Subscription ID",
            "watermarkText": "Choose an option",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions?api-version=2014-04-01",
                "jTokenPath": "value",
                "textProperty": "displayName,subscriptionId",
                "textTemplate": "{displayName} ({subscriptionId})",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            },
            "dropdownOptions": [
                {
                    "value": "dont_know_answer",
                    "text": "Not in the list"
                }
            ],
            "useAsAdditionalDetails": false,
            "required": true
        },
        {
            "id": "subscriptionid_details",
            "order": 10,
            "visibility": "SubscriptionId == dont_know_answer",
            "controlType": "textbox",
            "displayLabel": "Subscription ID",
            "watermarkText": "Provide your Subscription id",
            "required": false
        },
        {
            "id": "requesttype_details",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Select the Request type",
            "watermarkText": "Select the type of request",
            "dropdownOptions": [
                {
                    "value": "Activation Request",
                    "text": "Activation Request"
                },
                {
                    "value": "Extension Request",
                    "text": "Extension Request"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "requesttype_details1",
            "order": 4,
            "visibility": "requesttype_details == Activation Request",
            "controlType": "multilinetextbox",
            "displayLabel": "Error message encountered during activation (if applicable) ",
            "watermarkText": "Provide the error message encountered during activation (if applicable)",
            "required": false
        },
        {
            "id": "requesttype_details2",
            "order": 5,
            "visibility": "requesttype_details == Extension Request",
            "controlType": "textbox",
            "displayLabel": "Please provide the extension period",
            "watermarkText": " Provide the extension period",
            "required": false
        },
        {
            "id": "offertype_details",
            "order": 6,
            "controlType": "dropdown",
            "displayLabel": "Select the Offer type",
            "watermarkText": "Select the type of offer",
            "dropdownOptions": [
                {
                    "value": "Action Pack",
                    "text": "Action Pack"
                },
                {
                    "value": "Enterprise Agreement",
                    "text": "Enterprise Agreement"
                },
                {
                    "value": "Enterprise Dev/Test",
                    "text": "Enterprise Dev/Test"
                },
                {
                    "value": "Microsoft Azure Sponsored Offer",
                    "text": "Microsoft Azure Sponsored Offer"
                },
                {
                    "value": "MSDN Platforms subscribers",
                    "text": "MSDN Platforms subscribers"
                },
                {
                    "value": "Pay-As-You-Go",
                    "text": "Pay-As-You-Go"
                },
                {
                    "value": "Pay-As-You-Go Dev/Test",
                    "text": "Pay-As-You-Go Dev/Test"
                },
                {
                    "value": "Visual Studio Enterprise",
                    "text": "Visual Studio Enterprise"
                },
                {
                    "value": "Visual Studio Enterprise (BizSpark)",
                    "text": "Visual Studio Enterprise (BizSpark)"
                },
                {
                    "value": "Visual Studio Enterprise (MPN)",
                    "text": "Visual Studio Enterprise (MPN)"
                },
                {
                    "value": "Visual Studio Professional",
                    "text": "Visual Studio Professional"
                },
                {
                    "value": "Visual Studio Test Professional",
                    "text": "Visual Studio Test Professional"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other"
                }
            ],
            "required": true
        },
        {
            "id": "offertype_details2",
            "order": 7,
            "visibility": "offertype_details == dont_know_answer",
            "controlType": "textbox",
            "displayLabel": " Provide the Offer Type",
            "watermarkText": "Provide the Offer Type",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 8,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide a brief description of the issue",
            "watermarkText": "Provide a brief description of the issue",
            "useAsAdditionalDetails": true,
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
