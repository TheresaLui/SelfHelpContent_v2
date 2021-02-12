<properties
	pageTitle="Continuous Deployment of Bot"
	description="Scoping questions to capture more details about Continuous Deployment of Bot"
	authors="meetshamir"
	ms.author="saziz"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32688634"
	productPesIds="16152"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="840FBFC6-ED05-4F4C-945D-2D327E3FEC21"
	ownershipId="Compute_BotService"
/>
# Continuous Deployment of Bot
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Billing",
    "fileAttachmentHint": "Please upload screenshots that will help us understand the issue",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "infoBalloonText": "Enter the approximate time you started to see the error.",
            "required": true
        },
        {
            "id": "problem_end_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem stop? (If ongoing, leave this field blank)",
            "infoBalloonText": "Enter when the error stopped, or leave blank if the issue is ongoing.",
            "required": false
        },
		{
			"id": "error_advice",
			"order": 3,
			"controlType": "radioButtonGroup",
			"displayLabel": "Which of the following you need help with?",
			"radioButtonOptions": [
			    {
					"value": "advice",
					"text": "Advice on continuous deployment"
				},
				{
					"value": "configure",
					"text": "Issue with configuring deployment"
				},
				{
					"value": "disabling",
					"text": "Issue with disabling deployment"
				},
				{
					"value": "Other",
					"text": "Need help with something else"
				}
			],
			"required": true
		},
		{
			"id": "c1",
			"order": 4,
			"visibility":"error_advice == configure || error_advice == advice",
			"controlType": "radioButtonGroup",
			"displayLabel": "What source control system are you using for continuous deployment?",
			"radioButtonOptions": [
			    {
					"value": "azure",
					"text": "Azure Repos"
				},
				{
					"value": "github",
					"text": "GitHub"
				},
				{
					"value": "bitbucket",
					"text": "Bitbucket"
				},
				{
					"value": "local",
					"text": "Local Git"
				},
				{
					"value": "c1_other",
					"text": "Other"
				}
			],
			"required": true
		},
		{
			"id": "c2",
			"order": 5,
			"visibility":"c1 == c1_other",
			"controlType": "textbox",
			"displayLabel": "Please specify the source control system that you are using",
			"required": true
		},
		{
			"id": "c3",
			"order": 6,
			"visibility":"c1 == github || c1 == bitbucket",
			"controlType": "radioButtonGroup",
			"displayLabel": "Are you able to successfully authorize your app service?",
			"infoBalloonText":"For Bitbucket or GitHub, you should authorize Azure App Service to connect to your repository. You need to authorize with a source control service at least once",
			"radioButtonOptions": [
			    {
					"value": "no_auth",
					"text": "No, I face an issue with authorization"
				},
				{
					"value": "yes_auth",
					"text": "Yes, authorization is successful "
				}
			],
			"required": true
		},
		{
			"id": "c4",
			"order": 7,
			"visibility":"error_advice == configure || error_advice == advice",
			"controlType": "radioButtonGroup",
			"displayLabel": "What are you using as the build provider for your CI/CD?",
			"infoBalloonText":"If your existing Azure DevOps organization isn't listed, you may need to link it to your Azure subscription",
			"radioButtonOptions": [
			    {
					"value": "appservice",
					"text": "App Service Build Service"
				},
				{
					"value": "pipeline",
					"text": "Azure Pipelines"
				}
			],
			"required": true
		},
		{
			"id": "c5",
			"order": 8,
			"visibility":"c1 == azure",
			"controlType": "radioButtonGroup",
			"displayLabel": "Is your Azure DevOps organization linked to your subscription?",
			"infoBalloonText":"If your Azure DevOps organization isn't listed, make sure it's linked to your Azure subscription. For more information, see <a href='https://docs.microsoft.com/azure/devops/pipelines/apps/cd/deploy-webdeploy-webapps?view=azure-devops'> this </a>",
			"radioButtonOptions": [
			    {
					"value": "yes_azure",
					"text": "Yes, it is linked"
				},
				{
					"value": "no_azure",
					"text": "No, need assistance in linking Azure DevOps to our subscription"
				}
			],
			"required": true
			},
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional details, if you see an error message list it or you are looking for specific guidance.",
            "required": true,
            "useAsAdditionalDetails": true,
            "watermarkText": "Please provide as much details as possible"
        }
	]
}
---
