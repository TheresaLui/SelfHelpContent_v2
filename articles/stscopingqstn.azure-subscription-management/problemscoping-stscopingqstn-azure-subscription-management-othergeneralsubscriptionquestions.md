<properties
	pageTitle="Scoping questions for Other General Subscription Questions"
	description="Scoping questions for Other General Subscription Questions"
	authors="prdasneo"
	ms.author="prdasneo"
        selfHelpType="problemScopingQuestions"
	supportTopicIds="32454929"
	productPesIds="15660"
	cloudEnvironments="public"
        schemaVersion="1"
        articleId="e5b28325-284e-40ce-aa2b-d182995f93ea"
	ownershipId="ASMS_SubscriptionManagement"
/>
# Other General Subscription Questions
---
{
    "resourceRequired": false,
    "title": "Other General Subscription Questions",
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
            "id": "problem_description",
            "order": 2,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Problem Description",
            "watermarkText": "Provide any error message or additional information about your issue",
            "required": true,
            "hints": [
                {
                    "text": "If you would like to increase your compute cores subscription limit quota, please select the problem type <a href='https://ms.portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/newsupportrequest'>Compute/VM (cores/vCPUs) subscription limit increases</a> instead. This will allow our support team to more efficiently process your request."
                }
            ]
        },
        {
            "id": "additional_details1",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Additional Details",
            "watermarkText": "Select the type of issue",
            "dropdownOptions": [
                {
                    "value": "Support Case Submission Issue",
                    "text": "Support Case Submission Issue"
                },
                {
                    "value": "Other issue",
                    "text": "Other issue"
                }
            ],
            "required": true
        },
        {
            "id": "additional_details2",
            "order": 4,
            "visibility": "additional_details1 == Other issue",
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide the details of the issue",
            "required": true
        },
        {
            "id": "additional_details3",
            "order": 5,
            "visibility": "additional_details1 == Support Case Submission Issue",
            "controlType": "dropdown",
            "displayLabel": "Select the issue",
            "watermarkText": "Select the type of issue",
            "dropdownOptions": [
                {
                    "value": "Other issues",
                    "text": "Other issues"
                },
                {
                    "value": "Support tickets missing from the blade",
                    "text": "Support tickets missing from the blade"
                },
                {
                    "value": "Unable to add messages to a support ticket",
                    "text": "Unable to add messages to a support ticket"
                },
                {
                    "value": "Unable to create technical support request",
                    "text": "Unable to create technical support request"
                },
                {
                    "value": "Unable to reopen a closed ticket",
                    "text": "Unable to reopen a closed ticket"
                }
            ],
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
