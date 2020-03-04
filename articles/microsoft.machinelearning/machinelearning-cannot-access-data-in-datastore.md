
<properties 
    pageTitle="I cannot access my data or connect to a datastore"
    description="I cannot access my data or connect to a datastore"
    service="microsoft.machinelearning"
    resource="datastore"
    authors="SturgeonMi"
    ms.author="xunwan"
    selfHelpType="generic"
    supportTopicIds="32690860"
    resourceTags=""
    productPesIds="16644"
    cloudEnvironments="Public"
    articleId=" machinelearning-cannot-access-data-in-datastore"
	ownershipId="ASEP_ContentService_Placeholder"
/>

# Why I can’t access data or connect to a datastore?

There are five common reasons that might lead to this situation. The following steps below can help you identify the reason.

## Common reasons of why can’t access data or connect to a datastore

### Network issue

If you got this error message: "REQUEST_SEND_ERROR: Failed to send request to https://<ACTUAL_LINK_TO_DATASTORE>", please check if your network is functioning well.

### Different VNET

If you got this error message: "Error: Unable to access data. This might be because your data is stored behind a virtual network, the datastore credentials might not have sufficient privileges, or the storage account permissions might not be set up correctly", please check if your datastore is within a VNET.

If the data you want to access is behind a VNET, and you are not in the same VNET, you won’t be allowed to access the data from your current VNET.

### Authentication failure

If you got this error message: "Error when accessing datastore: Server failed to authenticate the request. Make sure the value of Authorization header is formed correctly including the signature.", please check your authentication information.

If the authentication credential provided for this datastore is incorrect, for example you are providing the wrong SAS token or Account key, you won’t be able to access the data.

### Don’t have permission

If you got this error message: "AuthorizationFailed: The client '<ACTUAL_ACCOUNT>' with object id '<ACTUAL_OBJECT_ID>' does not have authorization to perform action '<ACTUAL_ACTION_PERFORMED>' or the scope is invalid, If access was recently granted, please refresh your credentials.", please check your permissions. 

If it’s a credential-less datastore and your Role doesn’t have permission to access the data, you won’t be able to access the data via datastore.
The Role and permission is set by your admin. You can ask your admin to add corresponding permission for you.

### Backend data deleted

If you got this error message: "Error when accessing datastore: The specified container does not exist." Please validate if the data existed.

If the backend data container/data is deleted, then you can’t access the data.

## **Recommended Documents**

* [How to access data](https://docs.microsoft.com/azure/machine-learning/how-to-access-data)<br>
