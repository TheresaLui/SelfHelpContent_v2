<properties
	pageTitle="Issues in creating configuration (GitOps) on Arc enabled Kubernetes"
	description="Issues in creating configuration (GitOps) on Arc enabled Kubernetes"
	ms.author="shasb"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32739657"
	productPesIds="17112"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="a45d3434-4824-417f-b5b8-1dfc2c8a5377"
	ownershipId="AzureArc_HybridKubernetes"
/>

# Issues in creating configuration (GitOps) on Arc enabled Kubernetes

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
            "id": "versions",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Which version of Azure CLI, Kubernetes cluster are you running?",
            "watermarkText": "Run 'az -v; kubectl version' and paste the output of the command here",
            "required": true
        }, {
            "id": "agent_scheduling",
            "order": 3,
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
            "order": 4,
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
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        }
    ]
}
---
