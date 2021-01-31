<properties
  pagetitle="V2 - Mapping Data Flow Common Solutions"
  service=""
  resource=""
  ms.author="jaserano,rakatuko"
  selfhelptype="Generic"
  supporttopicids="32633535,32633532,32633537,32633533,32633536"
  resourcetags=""
  productpesids="15613"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="4041ad80-1861-9011-a7a2-828a98325d20"
  ownershipid="AzureData_DataFactory" />
# V2 - Mapping Data Flow Common Solutions

## **Performance Recommendations**:

**General Recommendations:**
If you are using SQL source, we recommend that you: 

- Analyze the dataflow for optimized partitioning. Refer to this [Optimized tab](https://docs.microsoft.com/azure/data-factory/concepts-data-flow-performance#optimize-tab) for more details.
- If 1==1 is being used in a join condition, we recommend instead that you use column value to compare.
- Debug clusters are intended to preview small data. Increase compute size in proportion to the payload being submitted.

**Recommended Partitions:**
Based on sources, we recommend the following partitionings:
- SQL Source > source partitioning
- File Base Source/Sink > default partitioning is best
- In intermediate transformations, avoid any explicit partitions other than source and sink.

## **Recommended Documents**

- [Mapping data flows in Azure Data Factory Overview](https://docs.microsoft.com/azure/data-factory/concepts-data-flow-overview)
- [Mapping data flow Datasets](https://docs.microsoft.com/azure/data-factory/concepts-data-flow-datasets)
- [Create Azure Data Factory data flow](https://docs.microsoft.com/azure/data-factory/data-flow-create)
- [Mapping data flow Debug mode](https://docs.microsoft.com/azure/data-factory/concepts-data-flow-debug-mode)
- [Execute data flow activity in Azure Data Factory](https://docs.microsoft.com/azure/data-factory/control-flow-execute-data-flow-activity)

**Data Flow Transformations**

- [Mapping data flow source transformation](https://docs.microsoft.com/azure/data-factory/data-flow-source)
- [Mapping data flow schema drift](https://docs.microsoft.com/azure/data-factory/concepts-data-flow-schema-drift)
- [Mapping data flow sink transformation](https://docs.microsoft.com/azure/data-factory/data-flow-sink)

**FAQ**

- [Azure Data Factory FAQ](https://docs.microsoft.com/azure/data-factory/frequently-asked-questions)
- [Feature Request](https://feedback.azure.com/forums/270578-azure-data-factory)
