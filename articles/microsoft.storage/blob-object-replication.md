<properties
	pageTitle="How to conduct object replication"
	description="How to conduct object replication"
	service="microsoft.storage"
	resource="storage"
	authors="siz"
	ms.author="siz"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32740858"
	resourceTags=""
	productPesIds="16459"
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	articleId="fec8434a-ee85-432e-a300-7cfb4369d056"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# How to conduct object replication

## **Recommended Steps**

### **Preview Conditions**

- A storage account can serve as the source account for up to two destination accounts
- The source and destination accounts may all be in different regions.
- Each rule defines a single source and destination container, and each source and destination container can be used in only one rule
- You can specify up to 10 replication rules for each replication policy
- After you create the replication policy, the destination container becomes read-only. Any attempts to write to the destination container fail with error code 409 (Conflict). However, you will be able to call Set Blob Tier API to move blobs in the destination container to a different access tier. You will also be able to delete these blobs. 

### **Frequently Asked Questions**

- [Prerequisites for object replication](https://docs.microsoft.com/azure/storage/blobs/object-replication-overview?tabs=powershell#prerequisites-for-object-replication)
- [How to register for the preview](https://docs.microsoft.com/azure/storage/blobs/object-replication-overview?tabs=powershell#register-for-the-preview)
- [How to create a replication policy and rules](https://docs.microsoft.com/azure/storage/blobs/object-replication-configure?tabs=portal#create-a-replication-policy-and-rules)
