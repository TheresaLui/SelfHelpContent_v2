<properties
	articleId="problemscopingques-blob-staticwebsite"
	pageTitle="Static Website Scoping Questions"
	description="tatic Website Scoping Questions"
	authors="annayak"
	ms.author="annayak"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32613339"
	productPesIds="16459"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>
# Static Website Issue
---
{
	"subscriptionRequired": true,
	"resourceRequired": true,
	"title": "Static Website Issues",
	"fileAttachmentHint": "",
	 "diagnosticCard": {
        "title": " Static Website Troubleshooter",
        "description": "Help us with a few inputs and give us couple of minutes to run automated diagnostics. We can help diagnose your problem without the need of opening a case.",
        "insightNotAvailableText": "Our troubleshooter did not detect any issues with your resource. Please ensure you provided the correct issue time and ServerRequestId."
    },
	"formElements": [{
			"id": "common_issues",
			"order": 1,
			"controlType": "dropdown",
			"displayLabel": "Select the problem type",
			"watermarkText": "Choose a problem",
			"dropdownOptions": [{
					"value": "Firewall_Support",
					"text": "Does storage firewall work with Static Website?"
				},
				{
					"value": "AzureAD_Support",
					"text": "Does Static Website support Azure AD authentication?"
				},
				{
					"value": "CustomDomain_Support",
					"text": "How to use custom domain with Static Website?"
				},
				{
					"value": "CustomSSL_Support",
					"text": "How to use custom SSL certificate with Static Website?"
				},
				{
					"value": "CustomHeaders_Support",
					"text": "How to add custom headers and rules with Static Website?"
				},
				{
					"value": "Redirection_Error",
					"text": "Why is site root not redirecting to the page set for \"index document name\" ?"
				},
				{
					"value": "Troubleshoot_Error",
					"text": "Troubleshoot a specific error"
				},
				{
					"value": "dont_know_answer",
					"text": "I have some other issue"
				}
			],
			"required": true,
			"diagnosticInputRequiredClients": "Portal,ASC"
		},
		{
			"id": "error_code_dropdown",
			"order": 2,
			"visibility": "common_issues == Troubleshoot_Error",
			"controlType": "dropdown",
			"displayLabel": "Http Error code",
			"watermarkText": "HTTP error of failed operation",
			"dropdownOptions": [{
					"value": "HTTP_400",
					"text": "HTTP 400"
				},
				{
					"value": "HTTP_401",
					"text": "HTTP 401"
				},
				{
					"value": "HTTP_403",
					"text": "HTTP 403"
				},
				{
					"value": "HTTP_404",
					"text": "HTTP 404"
				},
				{
					"value": "HTTP_409",
					"text": "HTTP 409"
				},
				{
					"value": "HTTP_500",
					"text": "HTTP 500"
				},
				{
					"value": "HTTP_503",
					"text": "HTTP 503"
				},
				{
					"value": "dont_know_answer",
					"text": "Other Error"
				}
			],
			"required": true,
			"diagnosticInputRequiredClients": "Portal,ASC"
		},
		{
			"id": "other_error_code",
			"visibility": "error_code_dropdown == dont_know_answer",
			"order": 3,
			"controlType": "textbox",
			"displayLabel": "Error code or message",
			"watermarkText": "Provide the error code you received.",
			"required": true,
			"diagnosticInputRequiredClients": "Portal,ASC"
		},
		{
			"id": "request_id",
			"order": 4,
			"visibility": "common_issues == Troubleshoot_Error",
			"controlType": "textbox",
			"displayLabel": "Storage server Request ID",
			"watermarkText": "Request ID of failed operation ending with 000000",
			"textPropertyRegex": "^([0-9A-Za-z]{8}[-][0-9A-Za-z]{4}[-][0-9A-Za-z]{4}[-][0-9A-Za-z]{4}[-][0-9A-Za-z]{6}[0]{6})$",
			"required": false,
			"diagnosticInputRequiredClients": "Portal,ASC"
		},
		{
			"id": "problem_start_time",
			"order": 100,
			"visibility": "common_issues == Troubleshoot_Error",
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem start?",
			"required": true,
			"diagnosticInputRequiredClients": "Portal,ASC"
		},
		{
			"id": "problem_description",
			"order": 1000,
			"controlType": "multilinetextbox",
			"displayLabel": "Description",
			"watermarkText": "Provide additional information about your issue",
			"required": true,
			"useAsAdditionalDetails": true
		}
	],
	"$schema": "SelfHelpContent"
}
---
