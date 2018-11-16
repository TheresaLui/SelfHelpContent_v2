<properties
	pageTitle="Custom DNS Issues"
	description="Custom DNS Issues"
	authors="ansi12"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32588505"
	productPesIds="15078"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Custom DNS Issues
---
{
	"resourceRequired": true,
	"title": "Custom DNS Issues",
	"fileAttachmentHint": "",
	"formElements": [{
			"id": "custom_dns_tsg",
			"order": 1,
			"controlType": "infoblock",
			"content": "Before submitting the case, please follow the steps in the <a href='https://hdinsight.github.io/ClusterCRUD/hdinsight-vnet'>Custom DNS trouble shooting guide</a> to troubleshoot issues with custom DNS setup. Make sure that the Azure recursive resolver IP is in your DNS server list."
		}, {
			"id": "hostname",
			"order": 2,
			"controlType": "multilinetextbox",
			"displayLabel": "ssh into the head node of the cluster and run the command: 'hostname -f'. Paste the output below",
			"required": false,
			"useAsAdditionalDetails": false,
			"hints": [{
					"text": "Command output"
				}
			]
		}, {
			"id": "nslookup",
			"order": 3,
			"controlType": "multilinetextbox",
			"displayLabel": "ssh into the head node of the cluster and run the command: 'nslookup headnode_fqdn', where 'headnode_fqdn' is the fully qualified domain name of the headnode. Paste the output below",
			"required": false,
			"useAsAdditionalDetails": false,
			"hints": [{
					"text": "Command output"
				}
			]
		}, {
			"id": "dig",
			"order": 4,
			"controlType": "multilinetextbox",
			"displayLabel": "ssh into the head node of the cluster and run the command: 'nslookup headnode_fqdn 168.63.129.16', where 'headnode_fqdn' is the fully qualified domain name of the headnode. Paste the output below",
			"required": false,
			"useAsAdditionalDetails": false,
			"hints": [{
					"text": "Command output"
				}
			]
		}, {
			"id": "problem_description",
			"order": 5,
			"controlType": "multilinetextbox",
			"displayLabel": "Please provide any other details relevant to the problem",
			"required": false,
			"useAsAdditionalDetails": true,
			"hints": [{
					"text": "Issue description."
				}
			]
		}, {
			"id": "learn_more_text",
			"order": 6,
			"controlType": "infoblock",
			"content": "<a href='https://hdinsight.github.io/ClusterCRUD/hdinsight-vnet'>Learn more</a> about about commonly faced issues with using Custom DNS on HDInsight"
		}
	]
}
---
