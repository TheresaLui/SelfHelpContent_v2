<properties
    pageTitle="Azure HDInsight Authentication Failure: Ambari in cluster with Enterprise Security Package"
    description="Azure HDInsight Authentication Failure: Ambari in cluster with Enterprise Security Package"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="TobyTu"
    ms.author="jaserano"
    displayOrder=""
    selfHelpType="Generic"
    supportTopicIds="32636436"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="07b6cb2e-a702-4e4f-889d-465f97389a5f"
	ownershipId="AzureData_HDInsight"
/>

# Azure HDInsight Authentication Failure: Ambari in cluster with Enterprise Security Package

## **Recommended Documents**

* [How To: Configure an HDInsight cluster with ESP by using Azure Active Directory Domain Services](https://docs.microsoft.com/azure/hdinsight/domain-joined/apache-domain-joined-configure-using-azure-adds)
* [How To: Authorize Users for Apache Ambari Views](https://docs.microsoft.com/azure/hdinsight/hdinsight-authorize-users-to-ambari)
* User groups specified during the cluster creation process are synchronized at that time. User synchronization occurs automatically once every hour. To synchronize the users immediately, or to synchronize a group other than the groups specified during cluster creation, please follow this [article](https://docs.microsoft.com/azure/hdinsight/hdinsight-sync-aad-users-to-cluster#use-the-apache-ambari-rest-api-to-synchronize-users)
* [How To: Configure Apache Hive policies in HDInsight with Enterprise Security Package](https://docs.microsoft.com/azure/hdinsight/domain-joined/apache-domain-joined-run-hive)
* On-premises Active Directory or Active Directory on IaaS VMs: If you are using federation with Active Directory Federation Services (AD FS), you must [enable password hash sync](https://docs.microsoft.com/azure/active-directory-domain-services/tutorial-create-instance). If federation is being used and password hashes are synced correctly, but you are getting authentication failures, check if cloud password authentication is enabled for the PowerShell service principal. [More Information](https://docs.microsoft.com/azure/hdinsight/domain-joined/apache-domain-joined-architecture#on-premises-active-directory-or-active-directory-on-iaas-vms)
* [FAQ:Azure HDInsight Security and Certificates](https://docs.microsoft.com/azure/hdinsight/hdinsight-faq#security-and-certificates)
