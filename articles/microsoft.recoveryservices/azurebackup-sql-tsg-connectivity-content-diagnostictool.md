<properties
	  pageTitle="Verify Network status using the diagnostic tool"
	  description="Verify Network status using the diagnostic tool"
      service="Microsoft.RecoveryServices"
      resource="Microsoft.RecoveryServices/vaults"
	  authors="chgonugu"
	  ms.author="chgonugu"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="4da09597-8885-4ea4-bb19-b51296465a53"
	  ownershipId="StorageMediaEdge_Backup"
/>

# Verify Network status using the diagnostic tool

Use network diagnostic tool to verify the network status by following below steps.

1. Download the zip file named TestAADCallsForWindows.zip from: https://risrajtest.blob.core.windows.net/customertest/TestAADCallsForWindows.zip 
2. Extract the files.
3. Open the command prompt and cd to extracted file location.
4. Run the command: PsExec -s -i cmd.exe
	It will open an elevated command prompt window that is running as Local System.
5. From the elevated window, cd to the extracted location again and then run the following command: TestAADCallsForWindows.exe ParallelRegistration
6. Trigger re-registration of VM from Azure portal. he above utility will wait for registration to be triggered.
7.Keep the command prompt window running till Registration failed/succeeded from portal and verify if the registration has succeeded or not.

