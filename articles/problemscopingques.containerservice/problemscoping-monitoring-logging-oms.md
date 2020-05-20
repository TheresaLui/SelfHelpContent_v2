<properties
                pageTitle="Monitoring and Logging/OMS Agent"
                description="Monitoring and Logging/OMS Agent"
                authors="ChiragPavecha"
                ms.author="chiragpa"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32637194"
                productPesIds="16450"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="problemscoping-monitoring-logging-oms"
	ownershipId="Compute_AzureKubernetesService"
/>
# Monitoring and Logging
---
{
                "$schema": "SelfHelpContent",
                "subscriptionRequired": true,
                "resourceRequired": true,
                "title": "OMS Agent",
                "fileAttachmentHint": "If OMS pod is in crashloop, please attach the output of **kubectl describe pods 'OMSpodname'**",
                "formElements": [
                 {
                    "id": "problem_start_time",
                    "order": 1,
                    "controlType": "datetimepicker",
                    "displayLabel": "When did the problem start?",
                    "required": true
                },
                {
                    "id": "getErrorMsg",
                    "order": 2,
                    "controlType": "multilinetextbox",
                    "displayLabel": "What error message did you receive while performing this operation, if any?",
                    "required": false
                  },
                  {
                  "id": "problem_description",
                  "order": 3,
                  "controlType": "multilinetextbox",
                  "displayLabel": "Description",
                  "useAsAdditionalDetails": true,
                  "required": true
                  }
                ]
}
---
