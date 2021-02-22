<properties
	pageTitle="Unable to apply configurations at scale on Azure Arc enabled Kubernetes resources using Azure Policy"
	description="Unable to apply configurations at scale on Azure Arc enabled Kubernetes resources using Azure Policy"
	ms.author="shasb"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32739655"
	productPesIds="17112"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="915a6938-f722-4fcd-a2c9-07712362497e"
	ownershipId="AzureArc_HybridKubernetes"
/>

# Unable to apply configurations at scale on Azure Arc enabled Kubernetes resources using Azure Policy

---

{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Issues in creating configuration (GitOps) on Arc enabled Kubernetes",
    "fileAttachmentHint": "Upload the output of running the az k8sconfiguration show command",
    "formElements": [{
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did you try to create a configuration on your Azure Arc enabled Kubernetes cluster?",
            "required": true
        }, {
            "id": "agent_scheduling",
            "order": 2,
            "controlType": "dropdown",
            "infoBalloonText": "Run 'kubectl get pods -n azure-arc' to verify that all agent pods are in a 'Running' state",
            "displayLabel": "Are all Azure Arc agent pods in a Running state?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [{
                    "value": "Yes",
                    "text": "Yes"
                }, {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "I don't know"
                }
            ],
            "required": true
        }, {
            "id": "flux_scheduling",
            "order": 3,
            "controlType": "dropdown",
            "infoBalloonText": "Run 'kubectl get pods -n your-operator-namespace' to verify that the flux operator pods are in a 'Running' state",
            "displayLabel": "Are all Flux operator pods in a Running state?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [{
                    "value": "Yes",
                    "text": "Yes"
                }, {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "I don't know"
                }
            ],
            "required": true
        }, {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        }
    ]
}
---
