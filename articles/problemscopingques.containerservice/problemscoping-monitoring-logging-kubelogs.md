<properties
                pageTitle="Monitoring and Logging/Kube Logs"
                description="Monitoring and Logging/Kube Logs"
                authors="ChiragPavecha"
                ms.author="chiragpa"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32637192"
                productPesIds="16450"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="problemscoping-monitoring-logging-kubelogs"
	ownershipId="Compute_AzureKubernetesService"
/>
# Monitoring and Logging
---
{
                "$schema": "SelfHelpContent",
                "subscriptionRequired": true,
                "resourceRequired": true,
                "title": "Kube Logs",
                "fileAttachmentHint": "",
                "formElements": [
                 {
                    "id": "problem_start_time",
                    "order": 1,
                    "controlType": "datetimepicker",
                    "displayLabel": "When did the problem start?",
                    "required": true
                },
                {
                    "id": "getEnablingAccessing",
                     "order": 2,
                      "controlType": "dropdown",
                      "displayLabel": "Do you have trouble with enabling or accessing the Kube logs?",
                      "watermarkText": "Choose an option",
                      "dropdownOptions": [
                        {
                          "value": "Enabling",
                          "text": "Enabling"
                        },{
                          "value": "Accessing",
                          "text": "Accessing"
                        },
                        {
                          "value": "dont_know_answer",
                          "text": "Other"
                        }
                        ],
                        "required": false
                  },
                  {
                    "id": "getCLIcheck",
                     "order": 3,
                      "visibility": "getEnablingAccessing == Enabling",
                      "controlType": "dropdown",
                      "displayLabel": "Did you try to enable the logging through Azure CLI?",
                      "watermarkText": "Choose an option",
                      "dropdownOptions": [
                        {
                          "value": "Yes",
                          "text": "Yes"
                        },{
                          "value": "No",
                          "text": "No"
                        }
                        ],
                        "infoBalloonText": "Read <a href='https://docs.microsoft.com/azure/azure-monitor/insights/container-insights-update-metrics#upgrade-per-cluster-using-azure-cli'>here</a> for enabling logging through CLI.",
                        "required": false
                  },
                  {
                    "id": "getErrorMsg",
                    "order": 4,
                    "controlType": "multilinetextbox",
                    "displayLabel": "What error message did you receive while performing this operation, if any?",
                    "required": false
                  },
                  {
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
