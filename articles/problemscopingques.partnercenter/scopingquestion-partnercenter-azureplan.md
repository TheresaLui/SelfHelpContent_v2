<properties
	pageTitle="Partner Center Azure plan request"
	description="Partner Center Azure plan request"
	authors="brentserbus"
	ms.author="brserbus"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32684682,32684680,32684681,32692604"
	productPesIds="15960,17003"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="scopingquestion_partnercenter_azureplan"
	clientIds="partnercenter"
	ownershipId="PartnerCenter_Billing_and_Invoicing"
/>
# Partner Center Azure plan request
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Partner Center Azure plan",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "pc_subscription_id",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Please provide the Azure plan subscription id you are asking about.",
            "watermarkText": "Provide the Azure plan subscription as a GUID",
            "required": false
        },
	{
            "id": "pc_iseligible",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Have you reviewed the eligibility criteria in the recommended steps and verified that you should be eligible for partner earned credit for your Azure subscriptions?",
            "dropdownOptions": [
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "Yes",
                    "text": "Yes"
                }
                ],
            "required": false
             },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Please provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "problem_start_time",
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "Start Time",
            "watermarkText": "When did your issue begin?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
