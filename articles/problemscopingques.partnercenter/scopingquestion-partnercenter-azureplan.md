<properties
	pageTitle="Partner Center Azure plan request"
	description="Partner Center Azure plan request"
	authors="brentserbus"
	ms.author="brserbus"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32725891,32725899,32692604"
	productPesIds="17012,17003"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="scopingquestion_partnercenter_azureplan"
	clientIds="partnercenter"
	ownershipId="PartnerCenter_Transact_and_Manage"

/>
# Partner Center Azure plan request
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Partner Center Azure plan",
    "fileAttachmentHint": "Please provide screenshots of the 'Role Assignments' page under this "Access control (IAM)" tab in Azure portal to verify access on the customers' Azure Plan subscription.",
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
            "id": "invoice_number",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Please provide the invoice number.",
            "watermarkText": "Invoice number",
            "required": false
        },
	{
            "id": "pc_iseligible",
            "order": 3,
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
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Please provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "problem_start_time",
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "Date of the first impacted invoice",
            "watermarkText": "When did your issue begin?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
