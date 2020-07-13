<properties
    pageTitle="Clustering technologies"
    description="Clustering technologies"
    service="Microsoft.SqlVirtualMachine"
    resource="SqlVirtualMachines"
    ms.author="ujpat,vadeveka,amamun"   
    authors="ujpat,vadeveka,AbdullahMSFT"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32740075"
    resourceTags="windowsSQL"
    productPesIds="16342"
    cloudEnvironments="public,fairfax, usnat, ussec, blackforest, mooncake"
    articleId="f57ac583-97a5-4dba-b3bc-df6ca8b9133c"
    ownershipId="AzureData_AzureSQLVM"
/>


# Clustering Technologies

If you are planning to deploy a SQL AG on Linux then you can follow : [SQL Server availability basics for Linux deployments](https://docs.microsoft.com/sql/linux/sql-server-linux-ha-basics?view=sql-server-ver15)<br> 

## Common Issues
* **Configure Pacemaker** 

  * Configure Pacemaker on [RHEL](https://docs.microsoft.com/sql/linux/sql-server-linux-availability-group-cluster-rhel?view=sql-server-ver15#configure-pacemaker)
  * Configure Pacemaker on [SLES](https://docs.microsoft.com/sql/linux/sql-server-linux-availability-group-cluster-sles?view=sql-server-ver15#install-and-configure-pacemaker-on-each-cluster-node)
  * Configure Pacemaker on [Ubuntu](https://docs.microsoft.com/sql/linux/sql-server-linux-availability-group-cluster-ubuntu?view=sql-server-ver15#install-and-configure-pacemaker-on-each-cluster-node)
    
  
* **Configure Fencing (STONITH)**:

  * Configure fencing on [RHEL](https://docs.microsoft.com/sql/linux/sql-server-linux-availability-group-cluster-rhel?view=sql-server-ver15#configure-pacemaker)
  * Configure fencing on [SLES](https://docs.microsoft.com/sql/linux/sql-server-linux-availability-group-cluster-sles?view=sql-server-ver15#install-and-configure-pacemaker-on-each-cluster-node)
  * Configure fencing on [Ubuntu](https://docs.microsoft.com/sql/linux/sql-server-linux-availability-group-cluster-ubuntu?view=sql-server-ver15#install-and-configure-pacemaker-on-each-cluster-node)


## **Recommended Documents**

* [Setup Clustering and High Availability on RHEL](https://docs.microsoft.com/sql/linux/sql-server-linux-availability-group-cluster-rhel?view=sql-server-ver15)<br>
* [Setup Clustering and High Availability on SLES](https://docs.microsoft.com/sql/linux/sql-server-linux-availability-group-cluster-sles?view=sql-server-ver15)<br>
* [Setup Clustering and High Availability on Ubuntu](https://docs.microsoft.com/sql/linux/sql-server-linux-availability-group-cluster-ubuntu?view=sql-server-ver15)<br>
