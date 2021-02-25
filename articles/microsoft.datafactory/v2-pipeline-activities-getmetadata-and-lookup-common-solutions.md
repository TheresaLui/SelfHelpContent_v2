<properties
  pagetitle="Getmetadata and lookup Common Solutions&#xD;"
  description="Getmetadata and lookup Common Solutions"
  service=""
  resource=""
  ms.author="hemin,keynesy"
  selfhelptype="Generic"
  supporttopicids="32680906"
  resourcetags=""
  productpesids="15613"
  cloudenvironments="blackforest,fairfax,public,usnat,ussec,mooncake"
  disableclouds=""
  articleid="df4efa80-976d-4657-bed7-40d0e1f7bc72"
  ownershipid="AzureData_DataFactory" />
# Getmetadata and lookup Common Solutions

## **GetMetadata: Best Practices**
- **DO NOT** use a large dataset that contains many items (e.g. files / folders or tables) as an input of GetMetadata activity,
  - The maximum size of returned metadata is **4 MB** (**hard limit**). 
  - Even if *modifiedDatetimeStart* or *modifiedDatetimeEnd* (file filter) is set to limit the output, GetMetadata activity will inevitably scan all files in a large dataset for modified time is not natively indexed by most files stores.

- **DO NOT** enable metadata options you don't use for better performance.

## **Lookup: Common mistakes and hard limitations**
- When query or stored procedure is used,
  - it **MUST return one and exact one result set**, otherwise, Lookup activity may fail.
  - as Lookup activity may retry internally due to transient issues, please make sure query or stored procedure is **idempotent**.
- Output parameter of stored procedure can't be returned as output of Lookup activity.
- The Lookup activity can return up to **5000 rows**; if the result set contains more records, the first 5000 rows will be returned.
- The Lookup activity output supports up to **4 MB** in size, activity will fail if the size exceeds the limit. 
- Currently, the longest duration for Lookup activity before timeout is **24 hours**.

## **How to parameterize GetMetadata and Lookup activity**
Please go back to the previous page and re-select problem type and subtype (***Authoring or Development Issues/Parameterization and Expression Language***) for more details.

## **Recommended Documents**
Please checkout [Get Metadata activity in Azure Data Factory](https://docs.microsoft.com/azure/data-factory/control-flow-get-metadata-activity) to learn more about,
- Supported file connectors and databases
- Supported metadata options
- Other limitations

Please checkout [Lookup activity in Azure Data Factory](https://docs.microsoft.com/azure/data-factory/control-flow-lookup-activity) to learn more about,
- Supported capabilities
- How to use Lookup activity output in subsequent activity
- Other limitations