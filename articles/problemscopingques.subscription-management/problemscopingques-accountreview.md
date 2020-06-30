<properties
	pageTitle="Subscription Management-Account Review"
	description="Subscription Management-Account Review"
	articleId="accountreview-problemscopingquestions"
	ms.author="prdasneo"
	authors="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32633817"
	productPesIds="15660"
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="ASMS_SubscriptionManagement"
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
      "id": "problem_description",
      "order": 2,
      "controlType": "multilinetextbox",
      "useAsAdditionalDetails": true,
      "displayLabel": "Problem Description",
      "watermarkText": "Please provide a detailed description of your problem",
      "required": true,
      "hints": [
                {
                    "text": "We will work on your case immediately and might call you to resolve your issue"
		 },
		{
                    "text": "Please take a look at your contact information <a href='https://account.azure.com/Profile'>here</a>, and update anything that might be incorrect"
                },
		 {
                    "text": "Please take a look at your billing information <a href='https://portal.azure.com/#blade/Microsoft_Azure_Billing/BillingMenuBlade/Payment'>here</a>, and update anything that might be incorrect"
                }
            ]
    },
    {
      "id": "student_details1",
      "order": 3,
      "controlType": "dropdown",
      "displayLabel": "Are you a Student, Employee, or Individual?",
      "watermarkText": "",
      "dropdownOptions": [
        {
          "value": "Student",
          "text": "Student"
        },
        {
          "value": "Working for a Company",
          "text": "Working for a Company"
        },
        {
          "value": "Using Azure as an individual",
          "text": "Using Azure as an individual"
        },
        {
          "value": "dont_know_answer",
          "text": "Other"
        }
      ],
      "required": true
    },
    {
      "id": "company_details",
      "order": 4,
      "controlType": "textbox",
      "displayLabel": "Company or University name",
      "watermarkText": "Provide your Company or University name",
      "required": false
    },
    {
      "id": "url_details",
      "order": 5,
      "controlType": "textbox",
      "displayLabel": "URL/Website of Company or University",
      "watermarkText": "Provide the URL/Website of your Company or University",
      "required": false
    },
    {
      "id": "detaileddesc_details",
      "order": 7,
      "controlType": "multilinetextbox",
      "displayLabel": "Detailed description of how Azure is being used",
      "watermarkText": "Provide a detailed description of how you are using, or plan to use Azure, to help us resolve your issue as quickly as possible.",
      "required": true
    }
  ],
  "$schema": "SelfHelpContent"
}
---
