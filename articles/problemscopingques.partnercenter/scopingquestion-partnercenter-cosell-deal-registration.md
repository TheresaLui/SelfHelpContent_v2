<properties
	pageTitle="Partner Center Cosell Deal Registration"
	description="Partner Center Cosell Deal Registration"
	authors="felicefan"
	ms.author="v-felice"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32740791,32740796,32740797,32740801,32740809"
	productPesIds="17004"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="scopingquestion_partnercenter_cosell_deal_registration"
	clientIds="partnercenter"
	ownershipId="PartnerCenter_Cosell"
/>
# Partner Center Cosell Deal Registration
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Partner Center Cosell Deal Registration",
    "fileAttachmentHint": "Please attach a screenshot of the issue or error you are having",
    "formElements": [
        {
            "id": "referral_or_engagement_ID",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Referral or Engagement ID (*mandatory for IP Co-sell program)",
            "watermarkText": "Please provide referral or engagement ID.",
            "required": false
        },
        {
            "id": "seller_ID",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Please provide the seller ID.",
            "watermarkText": "In Partner Center select Settings then Developer settings or in CPP select the Profile page then Partner Center account details section",
            "required": false
        },
        {
            "id": "solution_name",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Solution Name",
            "watermarkText": "Please provide the solution name.",
            "required": false
        },
        {
            "id": "solution_ID",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Solution ID",
            "watermarkText": "Please provide the solution ID.",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Please provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "problem_start_time",
            "order": 6,
            "controlType": "datetimepicker",
            "displayLabel": "Start Time",
            "watermarkText": "When did your issue begin?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
