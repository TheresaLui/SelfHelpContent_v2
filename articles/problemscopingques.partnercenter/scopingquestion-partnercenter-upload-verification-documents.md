<properties
	pageTitle="Partner Center Upload verification documents"
	description="Partner Center Upload verification documents"
    authors="brentserbus"
    ms.author="brserbus"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32730248"
	productPesIds="17000"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="scopingquestion_partnercenter_upload_verification_documents"
	clientIds="partnercenter"
	ownershipId="PartnerCenter_Accounts_Onboarding_Access"
/>
# PC Sample
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Partner Center Upload verification documents",
    "fileAttachmentHint": "Please upload your employment verification documents as .pdf or screen shots. Realize these uploads must be less than 8MB. Review the types of employment verification from the recommended steps.",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 2,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Details of the issue.",
            "watermarkText": "Provide additional information about your verification documents.",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
