<properties
	pageTitle="Provisioning or deleting Studio (classic) resources"
	description="Provisioning or deleting Studio (classic) resources"
	infoBubbleText="Provisioning or deleting Studio (classic) resources"
	service="microsoft.machinelearningstudioclassic"
	resource="studioclassic"
	authors="likebupt"
	ms.author="keli19"
	articleId="machinelearning-studioclassic-provisioningordeletingstudioclassicresources"
	selfHelpType="generic"
	supportTopicIds="32321856"
	productPesIds="15570"
	cloudEnvironments="public, usnat, ussec, fairfax"
	ownershipId="AzureML_AzureMachineLearning"
/>

# Provisioning or deleting Studio (classic) resources

## **Recommended Steps**

- Notebook feature has been shut down since April, 2020. For free workspaces, there is no way to recover the deleted notebooks; for paid workspaces, the notebook files are still stored in workspace blob storage, under Notebooks container, but it is difficult to recover them because the names are unreadble.
- If a workspace was deleted more than 90 days ago, there is no way to recover it
- When customer creates a workspace using the ARM template, the pending invitation will be sent to the workspace owner (customer’s account).However, the maximum limit of pending invitations is 100. Customer has 122 pending invitations from the backend log. Therefore, customers cannot list all workspaces. You could delete a couple of out-of-date workspaces, and this will cancel some of pending invitation. When the pending invitation is below 100, try to create new workspace again.
- A known issue of workspace deletion is: if you deleted a workspace before August 2020, and created a new workspace with the same name within 21 days, the new workspace can be normally used but cannot be found or deleted in azure portal. We have fixed this issue for workspaces created after August 2020. For workspaces created before August 2020, if you intend to delete it, please open a ticket and support team will help delete.

## **Recommended Documents**

Microsoft Azure Machine Learning Studio (classic) is a collaborative, drag-and-drop tool you can use to build, test, and deploy predictive analytics solutions on your data. Customers currently using or evaluating Machine Learning Studio (classic) are encouraged to try [Azure Machine Learning designer](https://docs.microsoft.com/azure/machine-learning/concept-designer), which provides drag and drop ML modules plus scalability, version control, and enterprise security.
