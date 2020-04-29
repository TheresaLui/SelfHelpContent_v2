<properties
	pageTitle="Azure Recovery Services Agent installation or registration issues"
	description="Azure Recovery Services Agent installation or registration issues"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder="4"
	selfHelpType="generic"
	supportTopicIds="32553287"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="9618140e-9906-4cb1-9b6b-5d99941d893a"
	ownershipId="StorageMediaEdge_Backup"
/>

# Azure Recovery Services Agent installation or registration issues

## **Recommended Steps**

- [Ensure there is network connectivity between MARS agent and Azure](https://aka.ms/AB-A4dp50) <br>
- Ensure **System Clock** on the protected system is configured to correct time zone <br>
- If you are trying to **reregister your server** to a vault, then: <br>
  - Ensure the agent is uninstalled on the server and it is deleted from portal <br> 
  - Use the same passphrase that was initially used for registering the server <br>
- Ensure your OS has the latest updates <br>
- [Ensure that the server has at least .Net Framework version 4.5.2 and higher](https://www.microsoft.com/download/details.aspx?id=30653)<br>
- [Invalid vault credentials provided: The file is either corrupted or does not have the latest information](https://aka.ms/AB-AA4dwts) <br>
- [The Microsoft Azure Recovery Service Agent was unable to connect to Microsoft Azure Backup](https://aka.ms/AB-A4dp50) <br>
- [Failed to set the encryption key for secure backups](https://aka.ms/AB-AA4dp56) <br>
- [The encryption passphrase stored on this computer is not correctly configured](https://aka.ms/AB-AA4dwto) <br>
