<properties
	pageTitle="Problems cancelling a job running in a quantum workspace"
	description="When you attempt to cancel a job, it continues to execute."
	infoBubbleText="Job continues to execute despite cancellation"
	service="microsoft.quantum"
	resource="workspaces"
	ms.author="dasto"
	displayOrder=""
	articleId=""
	diagnosticScenario=""
	selfHelpType=""
	supportTopicIds="quantum-unabletocanceljob"
	resourceTags=""
	productPesIds="17040"
	cloudEnvironments="public"
	ownershipId=""
/>

# After cancelling a job it continues to run

You may request to cancel a job after having submitted it, however job cancellations are not guaranteed.

Job cancellations should instead be treated as 'cancellation requests'. Additionally the behavior might differ based on the provider you are using.

## **Recommended Steps**

1. Please review our provider [documentation](https://github.com/MicrosoftDocs/quantum-docs-private/wiki/Azure-Quantum-provider) to establish whether your chosen provider supports cancellation requests
2. If your provider supports cancellation, retry your request as it can take several seconds or even minutes (depending on the provider) for the cancellation request to complete
3. If your issues persists, please record the time of your cancellation requests and raise a support case. A member of the team will help you troubleshoot further.

## **Recommended Documents**

*Please note that our documentation for Azure Quantum is in limited preview. Only customers currently in the limited preview can access the documentation resources linked.*
* [Job Submission with Azure Quantum](https://github.com/MicrosoftDocs/quantum-docs-private/wiki/Submit-jobs-to-Azure-Quantum-with-the-Comand-Line-Interface)