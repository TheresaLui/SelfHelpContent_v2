<properties
    selfHelpType = "generic"
    cloudEnvironments = "public, fairfax, blackforest, mooncake, usnat, ussec"
    ownershipId = "AzureData_SynapseAnalytics"
    service = "microsoft.synapse"
    resource = "bigDataPools"
    resourceTags = ""
    productPesIds = "15818"
    supportTopicIds = "32783918"
    displayOrder = ""
    diagnosticScenario = ""
    infoBubbleText = ""
    pageTitle = "How-To/Spark pool - Libraries and packages"
    description = "How-To/Spark pool - Libraries and packages"
    articleId = "synapse-cs-howto-sparkpoollibrariesandpackages.md"
    ms.author = "saltug"
/>

# How-To/Spark pool - Libraries and packages

## **Recommended Steps**

Spark pools in Azure Synapse include the following libraries that are available on the pools by default.
* [Spark Core](https://spark.apache.org/docs/latest/). Includes Spark Core, Spark SQL, GraphX, and MLlib.

* [Anaconda](https://docs.continuum.io/anaconda/)

* [.NET for Apache Spark](https://dot.net/spark)

Review the list of [Supported language and runtime versions](https://docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-version-support) for Apache Spark and dependent components

You can [add and manage additional libraries](https://docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-azure-portal-add-libraries) for Spark pool.

Review [```requirements.txt``` file format](https://docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-azure-portal-add-libraries#requirements-format) and [the pip freeze reference documentation](https://pip.pypa.io/en/stable/reference/pip_freeze/).

**Important**
* The packages listed in ```requirements.txt``` file for install or upgrade are downloaded from PyPi at the time of cluster startup.

* If the package you are installing is large or takes a long time to install, this affects the Spark instance startup time.

* Packages which require compiler support at install time, such as GCC, are not supported.

* Packages cannot be downgraded, only added or upgraded.


## **Recommended Documents**

* [Microsoft Spark Utilities](https://docs.microsoft.com/azure/synapse-analytics/spark/microsoft-spark-utilities?pivots=programming-language-csharp)

* [Build a machine learning app with Apache Spark MLlib](https://docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-machine-learning-mllib-notebook)

* [Use .NET for Apache Spark with Azure Synapse Analytics](https://docs.microsoft.com/azure/synapse-analytics/spark/spark-dotnet)

* [Spark.NET C# kernel features](https://docs.microsoft.com/azure/synapse-analytics/spark/spark-dotnet#sparknet-c-kernel-features)

 