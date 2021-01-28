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

* You can parameterize a linked service and pass dynamic values at run time. For example, parameterize database name or other properties. See [Parameterize Linked Services](https://docs.microsoft.com/azure/data-factory/parameterize-linked-services#supported-data-stores) for the list of supported linked service types. 
* If you hit any issue during publishing, click "Validate" or "Validate all" button to validate your payload. If anything shows up in the validation pane, click that item. It will navigate you to the problem. For the error message to fix it. 
* If your pipeline run can't run successfully:
  * Find the referenced linked service first. Try test connection in Linked Service. Follow the error message to fix your linked service if test connection failed. 
  * Find the referenced dataset, try to do "Preview data". Follow the error message to fix it if you see any failures. 
  * Try [debug run](https://docs.microsoft.com/azure/data-factory/iterative-development-debugging). You can also set breakpoint in your activity during debugging. 


## **Recommended Documents**

* [Pipelines and activities in Azure Data Factory](https://docs.microsoft.com/azure/data-factory/concepts-pipelines-activities)<br>
* [Linked services in Azure Data Factory](https://docs.microsoft.com/azure/data-factory/concepts-linked-services)<br>
* [Datasets in Azure Data Factory](https://docs.microsoft.com/azure/data-factory/concepts-datasets-linked-services)<br>
* [Integration runtime in Azure Data Factory](https://docs.microsoft.com/azure/data-factory/concepts-integration-runtime)<br>
* [Transform data in Azure Data Factory](https://docs.microsoft.com/azure/data-factory/transform-data)