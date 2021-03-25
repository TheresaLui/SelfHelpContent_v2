<properties
	pageTitle="Unable to connect Kubernetes cluster to Azure Arc"
	description="Unable to connect Kubernetes cluster to Azure Arc"
	ms.author="shasb"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32739656"
	productPesIds="17112"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="4a0d73bb-ab6c-4bb1-a048-1ae670980ce6"
	ownershipId="AzureArc_HybridKubernetes"
/>

# Unable to connect Kubernetes cluster to Azure Arc

---

{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Unable to connect Kubernetes cluster to Azure Arc",
    "fileAttachmentHint": "Upload the output of running the 'az connectedk8s connect' command with '--debug' parameter specified",
    "formElements": [{
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did you try to connect your Kubernetes cluster to Azure Arc?",
            "required": true
        }, {
            "id": "cluster_connectivity",
            "order": 2,
            "controlType": "dropdown",
            "infoBalloonText": "Run 'kubectl cluster-info' to verify connectivity to your Kubernetes cluster",
            "displayLabel": "Are you able to connect to your Kubernetes cluster?",
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
            "id": "network_requirements",
            "order": 3,
            "controlType": "dropdown",
            "infoBalloonText": "Network requirements can be found <a href='https://docs.microsoft.com/azure/azure-arc/kubernetes/connect-cluster#network-requirements'>here</a>",
            "displayLabel": "Does your environment meet the network requirements listed under Azure Arc documentation?",
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
            "id": "versions",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Which version of Azure CLI, Kubernetes cluster, and Helm are you running?",
            "watermarkText": "Run 'az -v; kubectl version; helm version' and paste the output of the command here",
            "required": true
        }, {
            "id": "outbound_proxy",
            "order": 7,
            "controlType": "dropdown",
            "infoBalloonText": "Docs on connecting using an outbound proxy server can be found <a href='https://docs.microsoft.com/azure/azure-arc/kubernetes/connect-cluster#connect-using-an-outbound-proxy-server'>here</a>",
            "displayLabel": "Does your cluster use a proxy server for outbound communication?",
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
            "order": 8,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        }
    ]
}
---
