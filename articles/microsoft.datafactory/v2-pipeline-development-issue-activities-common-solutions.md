<properties
  pagetitle="Azure Data Factory: V2 - Pipeline Development Issue - Activities Common Solutions"
  service=""
  resource=""
  ms.author="jaserano,vimals,haoc"
  selfhelptype="Generic"
  supporttopicids="32637149"
  resourcetags=""
  productpesids="15613"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="f5d17ec8-cfc2-4404-9472-537fa2a979b4"
  ownershipid="AzureData_DataFactory" />
# Azure Data Factory: V2 - Pipeline Development Issue - Activities Common Solutions

### **Common Issues**

* You can parameterize a linked service and pass dynamic values at run time. For example, parameterize the database name or other properties. For a list of supported linked service types, see [Parameterize Linked Services](https://docs.microsoft.com/azure/data-factory/parameterize-linked-services#supported-data-stores). 
* If you run into an issue during publishing, select **Validate** or **Validate all** to validate your payload. If anything shows up in the **Validation** pane, select that item. It will navigate you to the problem so that you can fix it. 

* If your pipeline run can't run successfully:
  * First, find the referenced linked service. In **Linked Service**, try a test connection. Follow the error message to fix your linked service if the test connection fails. 
  * Find the referenced dataset, by selecting **Preview data** if possible. Follow the error message to fix it if you see any failures. 
  * Try a [debug run](https://docs.microsoft.com/azure/data-factory/iterative-development-debugging). You can also set breakpoint in your activity during debugging. 


## **Recommended Documents**

* [Pipelines and activities in Azure Data Factory](https://docs.microsoft.com/azure/data-factory/concepts-pipelines-activities)<br>
* [Linked services in Azure Data Factory](https://docs.microsoft.com/azure/data-factory/concepts-linked-services)<br>
* [Datasets in Azure Data Factory](https://docs.microsoft.com/azure/data-factory/concepts-datasets-linked-services)<br>
* [Integration runtime in Azure Data Factory](https://docs.microsoft.com/azure/data-factory/concepts-integration-runtime)<br>
* [Transform data in Azure Data Factory](https://docs.microsoft.com/azure/data-factory/transform-data)
