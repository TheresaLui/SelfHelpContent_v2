<properties
	pageTitle="Scoping questions for Sponsorship Request"
	description="Scoping questions for Sponsorship Request"
	authors="prdasneo"
	ms.author="prdasneo"
  selfHelpType="problemScopingQuestions"
	supportTopicIds="32632958"
	productPesIds="15660"
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
  schemaVersion="1"
   articleId="SponsorshipRequest-problemscopingquestion"
	ownershipId="ASMS_SubscriptionManagement"
/>
#  Sponsorship Request
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Sponsorship Request",
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
            "id": "sponsorship_details",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Do you have an existing sponsorship?",
            "watermarkText": "Do you have an existing sponsorship?",
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
            "required": true
        },
        {
            "id": "sponsorship_details1",
            "order": 3,
            "visibility": "sponsorship_details == Yes",
            "controlType": "textbox",
            "displayLabel": " Provide the email ID approved for sponsorship",
            "watermarkText": "Provide the email ID approved for sponsorship",
            "required": false
        },
        {
            "id": "sponsorship_details2",
            "order": 4,
            "visibility": "sponsorship_details == Yes",
            "controlType": "multilinetextbox",
            "displayLabel": " Provide the list of subscriptions you want to convert to sponsorship",
            "watermarkText": "Provide the list of subscriptions you want to convert to sponsorship",
            "required": true
        },
        {
            "id": "sponsorship_details3",
            "order": 5,
            "visibility": "sponsorship_details == Yes",
            "controlType": "datetimepicker",
            "displayLabel": " Start Date of the sponsorship",
            "watermarkText": "Provide the start date of the sponsorship",
            "required": false
        },
        {
            "id": "sponsorship_details4",
            "order": 6,
            "visibility": "sponsorship_details == Yes",
            "controlType": "datetimepicker",
            "displayLabel": " End Date of the sponsorship",
            "watermarkText": "Provide the end date of the sponsorship",
            "required": false
        },
        {
            "id": "sponsorship_details5",
            "order": 7,
            "visibility": "sponsorship_details == Yes",
            "controlType": "textbox",
            "displayLabel": " Total monetary credit of the Sponsorship offered",
            "watermarkText": "Provide the total monetary credit of the Sponsorship offered",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 8,
            "controlType": "multilinetextbox",
            "displayLabel": "Brief description of your request",
            "watermarkText": "Please provide a brief description of your request",
            "useAsAdditionalDetails": true,
            "required": true,
            "hints": [
                {
                    "text": "Note: Attach the email confirmation along with this request in the file upload section"
                }
            ]
        },
        {
            "id": "sponsorship_details6",
            "order": 9,
            "visibility": "sponsorship_details == No",
            "controlType": "multilinetextbox",
            "displayLabel": "Additional details (if any)",
            "watermarkText": "Provide additional details (if any)",
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---
