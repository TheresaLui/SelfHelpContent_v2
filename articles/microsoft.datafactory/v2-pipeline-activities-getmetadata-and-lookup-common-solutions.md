<properties
  pagetitle="Getmetadata and lookup Common Solutions"
  description="Getmetadata and lookup Common Solutions"
  service=""
  resource=""
  ms.author="keynesy"
  selfhelptype="Generic"
  supporttopicids="32680906"
  resourcetags=""
  productpesids="15613"
  cloudenvironments="blackforest,fairfax,public,usnat,ussec,mooncake"
  disableclouds=""
  articleid="df4efa80-976d-4657-bed7-40d0e1f7bc72"
  ownershipid="AzureData_DataFactory" />
# Getmetadata and lookup Common Solutions

### **GetMetadata: Best Practices**
- Do not use a large dataset that contains many files, folders, or tables as an input of GetMetadata activity,
  - The maximum size of returned metadata is 4 MB (hard limit).
  - Even if *modifiedDatetimeStart* or *modifiedDatetimeEnd* (file filter) is set to limit the output, GetMetadata activity will inevitably scan all files in a large dataset for modified time is not natively indexed by most files stores.

- Do not enable metadata options you don't use for better performance.

### **Lookup: Common mistakes and hard limitations**
- When query or stored procedure is used, it:
  - Must return one and exact one result set, otherwise, Lookup activity may fail.
  - Should be idempotent, as Lookup activity may retry internally due to transient issues.
- Output parameter of stored procedure can't be returned as output of Lookup activity.
- The Lookup activity can return up to 5000 rows; if the result set contains more records, the first 5000 rows will be returned.
- The Lookup activity output supports up to 4 MB in size, activity will fail if the size exceeds the limit. 
- Currently, the longest duration for Lookup activity before timeout is 24 hours.

### **How to parameterize GetMetadata and Lookup activity**
Go back to the previous page and re-select problem type and subtype (*Authoring or Development Issues/Parameterization and Expression Language*) for more details.

## **Recommended Documents**
Check out [Get Metadata activity in Azure Data Factory](https://docs.microsoft.com/azure/data-factory/control-flow-get-metadata-activity) to learn more about,
- Supported file connectors and databases
- Supported metadata options
- Other limitations

Check out [Lookup activity in Azure Data Factory](https://docs.microsoft.com/azure/data-factory/control-flow-lookup-activity) to learn more about,
- Supported capabilities
- How to use Lookup activity output in subsequent activity
- Other limitations
