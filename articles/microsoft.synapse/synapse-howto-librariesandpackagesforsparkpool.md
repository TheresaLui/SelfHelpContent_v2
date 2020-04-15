<properties
	selfHelpType = "generic"
	cloudEnvironments = "public, fairfax, blackforest, mooncake"
	ownershipId = "AzureData_SQLDataWarehouse"
	service = "microsoft.synapse"
	resource = "bigDataPools"
	resourceTags = ""
	productPesIds = "15818"
	supportTopicIds = "32738775"
	displayOrder = ""
	diagnosticScenario = ""
	infoBubbleText = ""
	pageTitle = "How-To/Libraries and packages for Spark pool"
	description = "How-To/Libraries and packages for Spark pool"
	articleId = "synapse-howto-librariesandpackagesforsparkpool"
	authors = "saltug"
	ms.author = "saltug"
/>

# How-To/Libraries and packages for Spark pool

## **Recommended Steps**

Spark pools in Azure Synapse include the following libraries that are available on the pools by default.
* [Spark Core](https://spark.apache.org/docs/latest/). Includes Spark Core, Spark SQL, GraphX, and MLlib.
* [Anaconda](https://docs.continuum.io/anaconda/)
* [.NET for Apache Spark](https://dot.net/spark)

Review the list of [Supported language and runtime versions](https://review.docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-version-support) for Apache Spark and dependent components

You can [add and manage additional libraries](https://review.docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-azure-portal-add-libraries) for Spark pool.

Review [```requirements.txt``` file format](https://review.docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-azure-portal-add-libraries?branch=release-ignite-arcadia#requirements-format) and [the pip freeze reference documentation](https://pip.pypa.io/en/stable/reference/pip_freeze/).

**Important**
* The packages listed in ```requirements.txt``` file for install or upgrade are downloaded from PyPi at the time of cluster startup.
*  If the package you are installing is large or takes a long time to install, this affects the Spark instance start up time.
* Packages which require compiler support at install time, such as GCC, are not supported.
* Packages can not be downgraded, only added or upgraded.


## **Recommended Documents**

* [Build a machine learning app with Apache Spark MLlib](https://review.docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-machine-learning-mllib-notebook)
* [Use .NET for Apache Spark with Azure Synapse Analytics](https://review.docs.microsoft.com/azure/synapse-analytics/spark/spark-dotnet?branch=release-ignite-arcadia)
* [Spark.NET C# kernel features](https://review.docs.microsoft.com/en-us/azure/synapse-analytics/spark/spark-dotnet?branch=release-ignite-arcadia#sparknet-c-kernel-features)