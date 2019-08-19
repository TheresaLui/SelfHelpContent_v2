<properties
	pageTitle="Subscription Management - Account Review"
	description="Subscription Management - Account Review"
	articleId="accountreview-problemscopingquestions"
	ms.author="prdasneo"
	authors="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32607561"
	productPesIds="15660"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Account Review
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Account review",
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
            "id": "student_details1",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Are you a student?",
            "watermarkText": "",
            "dropdownOptions": [
                {
                    "value": "Working for a Company?",
                    "text": "Working for a Company?"
                },
                {
                    "value": "Using Azure as an individual?"
                    "text": "Using Azure as an individual?"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other"
                }
            ],
            "required": true
        },
        {
            "id": "student_details2",
            "order": 3,
            "visibility": "student_details1 == dont_know_answer",
            "controlType": "textbox",
            "displayLabel": "Please provide the details",
            "required": false
        },
        {
            "id": "company_details",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Company or University name",
            "watermarkText": "Provide the Company/University name",
            "required": false
        },
        {
            "id": "url_details",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "URL/Website of Company or University",
            "watermarkText": "Provide the URL/Website of Company or University",
            "required": false
        },
        {
            "id": "phone_details",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "Phone number where you can be contacted",
            "watermarkText": "Provide the Phone number where you can be contacted",
            "infoBalloonText": " Verify your phone/contact details <a href='https://portal.azure.com/#blade/Microsoft_Azure_Billing/BillingMenuBlade/Overview'>here</a>.",
            "required": false
        },
        {
            "id": "detaileddesc_details",
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "Detailed description of how Azure is being used",
            "watermarkText": "Provide the detailed description of how Azure is being used",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 8,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Problem Description",
            "watermarkText": "",
            "required": true
            }
    ],
    "$schema": "SelfHelpContent"
}
---
