<properties
	pageTitle="Debug issues with bot conversation flow or logic"
	description="Debug issues with bot conversation flow or logic"
	service="Microsoft.BotService"
	resource="botServices"
	authors="jwiley84,jiruss,dandriscoll,meetshamir"
	ms.author="v-jewail,jiruss,dandris,saziz"
	displayOrder="101"
	selfHelpType="resource"
	supportTopicIds="32688620"
	resourceTags=""
	productPesIds="16152"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	articleId="F8BF1475-F6AD-4B46-BBE0-6EFE638DDC9F"
	ownershipId="Compute_BotService"
/>

# Debug Bot Conversation

### Prerequisites

1. [Download and install the Bot Framework Emulator](https://github.com/Microsoft/BotFramework-Emulator/releases)
2. [Download and install Visual Studio Code or Visual Studio (Community Edition or above)](https://code.visualstudio.com/Download)

### Debug a JavaScript bot using breakpoints in Visual Studio Code

In Visual Studio Code, you can set breakpoints and run the bot in debug mode to step through your code. To set breakpoints in VS Code, do the following:

1. Launch VS Code and open your bot project folder
2. From the menu bar, click **Debug** and click **Start Debugging**. If you are prompted to select a runtime engine to run your code, select **Node.js**. At this point, the bot is running locally.
3. Click the **.js** file and set breakpoints as necessary. In VS Code, you can set breakpoints by hovering your mouse over the column to the left of the line numbers. A small red dot will appear. If you click on the dot, the breakpoint is set. If you click the dot again, the breakpoint is removed.
4. Start the Bot Framework Emulator and connect to your bot as described in the Debug with the Bot Framework Emulator section
5. From the emulator, send your bot a message (for example, send the message "Hi"). Execution will stop at the line where you place the breakpoint.

### Debug a C# bot using breakpoints in Visual Studio

In Visual Studio (VS), you can set breakpoints and run the bot in debug mode to step through your code. To set breakpoints in VS, do the following:

1. Navigate to your bot folder and open the **.sln** file. This will open the solution in VS.
2. From the menu bar, click **Build** and click **Build Solution**
In the **Solution Explorer**, click the **.cs** file and set breakpoints as necessary. This file defines your main bot logic. In VS, you can set breakpoints by hovering your mouse over the column to the left of the line numbers. A small red dot will appear. If you click on the dot the breakpoint is set. If you click the dot again the breakpoint is removed.
4. From the menu, click **Debug** and click **Start Debugging**. At this point, the bot is running locally.
5. Start the Bot Framework Emulator and connect to your bot as described in the section above
6. From the emulator, send your bot a message (e.g.: send the message "Hi"). Execution will stop at the line where you place the breakpoint.

### Connecting to the emulator

1. To connect to a bot running locally and click **Open bot**. Add the port number your copied earlier into the following URL and paste the updated URL in the Bot URL bar: `http://localhost: **port number** /api/messages`
2. Send a message to your bot and the bot should respond back. You can click on the message bubble within the conversation window and inspect the raw JSON activity using the **INSPECTOR** feature to the right side of the window. When selected, the message bubble will turn yellow and the activity JSON object will be displayed to the left of the chat window. The JSON information includes key metadata, including the channel ID, activity type, conversation ID, the text message, endpoint URL, and so on. You can inspect activities sent from the user, as well as activities the bot responds with.
3. You can also inspect the JSON responses from LUIS and QnA. Using a bot with a connected language service, you can select **trace** in the LOG window to the bottom right. 

    - With a connected LUIS service, you'll notice that the trace link specifies **Luis Trace**. When selected, you'll see the raw response from your LUIS service, which includes intents, entities along with their specified scores. You also have the option to re-assign intents for your user utterances.
    - With a connected QnA service, the log will display **QnA Trace**, and when selected you can preview the question and answer pair associated with that activity, along with a confidence score. From here, you can add alternative question phrasing for an answer.

## **Recommended Documents**

* [How to troubleshoot bots](https://docs.microsoft.com/azure/bot-service/bot-service-troubleshoot-general-problems?view=azure-bot-service-4.0)
