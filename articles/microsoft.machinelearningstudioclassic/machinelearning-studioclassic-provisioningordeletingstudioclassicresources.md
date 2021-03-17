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

- The Notebook feature has been shut down since April, 2020. For free workspaces, there is no way to recover the deleted notebooks. For paid workspaces, the notebook files are still stored in workspace blob storage, under Notebooks container, but it is difficult to recover them because the names are unreadable.
- Be careful when deleting any resources in your workspace, since there is no way to restore user-deleted resources.
- When a customer creates a workspace using the ARM template, the pending invitation will be sent to the workspace owner (that is, the customer’s account). However, if the pending invitations exceed the maximum limit of 100, the full list of workspaces won't be shown. By deleting a couple of out-of-date workspaces, the customer can cancel some of pending invitations. When the pending invitations are below 100, they can try to create a new workspace.
- Known issue: If you deleted a workspace before August 2020, and created a new workspace with the same name within 21 days, the new workspace can be used normally, but you won't be able to find or delete it in the Azure portal. We have fixed this issue for workspaces created after August 2020. For workspaces created before August 2020, if you intend to delete it, open a ticket and the support team will help you delete it.

## **Recommended Documents**

Microsoft Azure Machine Learning Studio (classic) is a collaborative, drag-and-drop tool you can use to build, test, and deploy predictive analytics solutions on your data. Customers currently using or evaluating Machine Learning Studio (classic) are encouraged to try [Azure Machine Learning designer](https://docs.microsoft.com/azure/machine-learning/concept-designer), which provides drag and drop ML modules plus scalability, version control, and enterprise security.
