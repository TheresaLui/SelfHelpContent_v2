<properties
	pageTitle="Kubernetes Prerequisites for SQL Managed Instance Azure Arc"
	description="Kubernetes Prerequisites for SQL Managed Instance Azure Arc"
	infoBubbleText="Kubernetes Prerequisites for SQL Managed Instance Azure Arc"
	service="microsoft.azuredata"
	resource="sqlmanagedinstances"
	ms.author="amigan,jopilov,prmadhes"
	displayOrder=""
	articleId="b6ab6c55-f018-448a-a50c-77e026357cbc"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32744007"
	resourceTags=""
	productPesIds="17125"
	cloudEnvironments="Public, fairfax, usnat, ussec"
	ownershipId="AzureData_Managed_Instance_Azure_Arc"
/>

# Kubernetes Prerequisites for SQL Managed Instance Azure Arc

Most users are able to resolve their prerequisites setup kubernetes issues for the deployment of SQL Managed Instance Azure Arc using the recommended documents below.

## **Recommended Steps**

- **Hardware requirements**:

   Minimum hardware requirements for Managed Instance Azure Arc are the following:

  - 8 vCPU
  - 32 GB RAM
  - 200 GB Storage
  - SSH Port 22 open

- **Cluster Prerequisites:**

  To evaluate Azure Arc enabled data services you will need to have a Kubernetes cluster deployed. The following deployment options have been tested:

  - Azure Kubernetes Service (AKS)
  - Azure Kubernetes Engine (AKE) on Azure Stack
  - OpenShift Container Platform (OCP) 4.2+
  - Azure RedHat OpenShift (ARO)
  - Open source, upstream Kubernetes typically deployed using **kubeadm**
  - AWS Elastic Kubernetes Service (EKS)

  **Note:** The tested version of Kubernetes is 1.14+.

- **Client tools prerequisites:**

  - [Install client tools for deploying and managing Azure Arc enabled data services](https://docs.microsoft.com/azure/azure-arc/data/install-client-tools)

- **Review the deployment:**

  Once deployment is complete, you can list the pods that have been deployed using the following command. These names are fixed when you use the script.

   ```bash
   kubectl get pods -n <namespace>
   ```

## **Recommended Documents**
* [Connectivity Modes and Requirements for Azure Arc Data Services](https://docs.microsoft.com/azure/azure-arc/data/connectivity)

* [Storage Configuration for Kubernetes](https://docs.microsoft.com/azure/azure-arc/data/storage-configuration)

* [Troubleshooting Kubernetes Clusters](https://kubernetes.io/docs/tasks/debug-application-cluster/debug-cluster/)

* [Create a Kubernetes cluster using kubeadm](https://github.com/microsoft/sql-server-samples/tree/master/samples/features/sql-big-data-cluster/deployment/kubeadm/ubuntu)

* [Troubleshooting kubeadm](https://kubernetes.io/docs/setup/production-environment/tools/kubeadm/troubleshooting-kubeadm/)

* [Cluster Networking](https://kubernetes.io/docs/concepts/cluster-administration/networking/)