# Create an Solution 2.0 article

Use this document to get started constructing Apollo Solution 2.0 articles. Here, we'll describe the article structure,  the components within that structure, and the basic requirements for building a compliant solution. For a complete description of Apollo, see the ![**Overview**](..assets/articles/Overview.md).


## Get started

- To create a solution from scratch, [download the raw format of the Apollo template in Markdown](https://github.com/Azure/SelfHelpContent/blob/master/documents/Apollo-template/Apollo-template.md). Alternatively, you can create an Apollo solution in Elixir and simply choose the components you want in your solution (versus typing the schema).
- Include all **required** components in the order they appear, as described in ![Basic structure of an Apollo solution](##_Basic_structure_of_an_Apollo_solution)
- For ideas on how to write an article, see also ![**Template and examples**](..assets/articles/TemplateExamples.md).
- Format your article in Markdown, unless XML is specifically called for.
- Review the [**Rules**](#_Rules) to avoid validation warnings and errors. Rules are in place to ensure your solution meets Microsoft standards for writing style, formatting, links, and accessibility.

## Basic structure of an Apollo solution

| **Required** | **Description** |
| --- | --- |
|Properties | Contains the metadata of the article |
|Internal title | Internal only (not customer-facing) component used by the Azure self-help portal |
|Customer-facing title | Provides context for your Apollo solution |
|Body | Main canvas of the article. **At minimum**, must contain an introduction and one or more solution components: diagnostics, Azure Monitor charts, video solutions, images, procedures, tables, and AzureKB article links


## Properties section

The properties section is required and contains the metadata of the article. All self-help articles must start with a **properties** section. For details about property metadata, see the table in the following section.

- Some properties are mandatory, others are optional. However, we ask that you include all properties and assign an empty string ("") as the value for properties you aren't using.
- Neither the order of the properties, spaces, or capitalization matters
- For properties that support multiple values, separate them using commas

    **Example of schema**

      <properties
          pageTitle="_Apollo\_article\_description_"<br>
          description="_Apollo\_article\_description_"<br>
          ms.author="_your\_name_"<br>
          displayOrder=""<br>
          articleId="0008d965-e21e-4e73-80ef-0ccc0765fb0c"<br>
          selfHelpType="Apollo"<br>
          supportTopicIds="7d8fb79f-7fbc-7125-b4dc-3060a75a755d"<br>
          productPesIds="16342,16065,15797,16454,16470"<br>
         cloudEnvironments="public"<br>
         ownershipId="b6015c21-c91a-4248-8d13-426894cd5140"<br>

       />

## Properties metadata

| Tag                | Description                                                                                                         | Required                                                                                 | Notes                                                                                                                                                                                                                                    | Example                                                                             |
|--------------------|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| pageTitle          | Name of the issue for troubleshoot content                                                                          | Yes                                                                                      | * This will not appear on the portal, it is metadata only  * This can only be one sentence - do not include periods or commas                                                                                                            | * Database Connectivity issue due to invalid credentials detected  * VM boot error  |
| description        | Name of the issue or any other description you would like.                                                          | Yes                                                                                      | This will not appear on the portal, it is metadata only                                                                                                                                                                                  | * IsBadPassword  * Virtual machine failed to boot with error code 0xc000000e        |
| ms.author          | Microsoft alias for the author                                                                                      | Yes                                                                                      | Microsoft alias of the person who wrote or last edited the documen                                                                                                                                                                       | * bernardm  * ramakk                                                                |
| displayOrder       | Not applicable to Insights                                                                                          | Only for articles displayed in the Help and Support blade (aka Troubleshoot blade)       |                                                                                                                                                                                                                                          |                                                                                     |
| articleId          | Unique identifier for the article                                                                                   | Yes                                                                                      | * MUST be unique for all Insight articles  * We highly recommend using the file name (which by default is also unique)                                                                                                                   | * isbadpassword * errorcod-e0xc000000e                                              |
| selfHelpType       | Set the value to “Apollo”                                                                                           | Yes                                                                                      |                                                                                                                                                                                                                                          |                                                                                     |
| supportTopicIds    | Support Topic Ids for which this content will be presented in case submission                                       | Only for Diagnostic articles and articles that will be presented during case submission  | * Must match a valid support topic for the Resource Provider and Resource Type  * Must match the support topic Id for which a Diagnostic Scenario was added in SEAM  * Can have multiple, comma separated values                         |                                                                                     |
| productPesIds      | Product Id(s) for the service for which the article will be presented                                               | Yes                                                                                      | * Must match a valid PesId for the Resource Provider and Resource Type  * In the case of diagnostics articles, it must match the PesId for which a Diagnostic Scenario was added in SEAM  * Can have multiple, comma separated values    | * "14749"  * "14749, 15571"                                                         |
| resourceRequired   |                                                                                                                     |                                                                                          |                                                                                                                                                                                                                                          |                                                                                     |
| cloudEnvironments  | Indicates if the content specific to a certain cloud. Possible values: "public, blackForest, fairfax and mooncake"  | Yes                                                                                      | * Can have multiple, comma separated values                                                                                                                                                                                              | * "public"  * "public, fairfax"                                                     |
| ownershipId        | Indicates the ownershipId who is responsible for this selfhelp asset                                                | Yes                                                                                      |                                                                                                                                                                                                                                          | ownershipId="Compute_BotService"                                                    |


## Internal title

Internal-only title **required** for internal reference. Level 1 heading. Use the following Markdown format.



## Customer-facing title

Required. Level 2 heading that describes the article contents, preferably in 10 words or less. The title and provides necessary context to the customer and reassurance that the solution targets their concern. Use sentence capitalization: Capitalize only the first word and any product, feature, or service names. Start with an active verb (such as resolve, enable, learn, troubleshoot, etc.). Do not add **bold** formatting as headings are automatically bolded.

**Examples:**

- "Troubleshoot High CPU Usage for your Virtual Machines"
- "Troubleshoot most commonly occurring performance issues using diagnostics and recommended document links below."
- "Learn How to Enable Auditing for your SQL DB"
- "Enable AD DS Authentication for Azure Files and Windows Virtual Desktop"


## Body section<br>
The body comes immediately after the customer-facing title and contains the _entire article contents_. Think of the body section as a canvas where you can place any combination of content and solution components. Always start with a brief [introduction](##_Introduction) that lets the customer know what they can expect from the solution.

**At minimum, your Apollo solution article must include the following**:<br>
- For a **solution-based article** , the body contains a solution that specifically addresses the stated **issue**.
- For a **how-to article** , the body contains **conceptual** or **procedural** information (in text or video).

## Introduction
  
In every article, explicitly state how the solution addresses a particular problem, or summarize the article. 
The introduction sets context and expectations for your customer and reassures them that they are on the correct page.

**Examples:**

- "Resolve issues related to configuring NetApps by reviewing the following solutions."
- "Identify and resolve causes of high CPU usage for an Azure Virtual Machine with the following diagnostics, 
videos, and relevant help links."
- "Learn how to adjust resource limits for NetApp files using the following procedure."
- "Review the following videos to understand the basics of continuous integration in DevOps."
- "Learn how to deploy Azure Monitor for Windows Virtual Machine (WVD) using the following video."

## Solution components

In addition to text, Apollo articles can include any of the following solution components:
- Diagnostics
- Metrics
- Videos
- Images
- Tables
- Procedures
- AzureKB and document links

The following sections describe each component and provide examples and schema for each.

## Diagnostics

Diagnostics are an optional feature of Azure Cloud Services that let you diagnose and collect data on the customer's deployed application. 
When you include a diagnostic in your solution, explain what it is and what information it's gathering, and how the customer can use that information to address their issue.

- Level 3 heading required
- If you have more than one diagnostic mapped against the support topic in SEAM and you are migrating the experience to Apollo, provide the symptomdIds as comma-separated list as shown in the following example.
- List diagnostics in the order you want the results to be displayed. Azure portal prioritizes the presented results for the first diagnostic mapped to the first symptomId. If no insight is found or the first diagnostic failed/timed-out, the portal proceeds to get the insight from the second diagnostic, and so on.


**Diagnostics schema definitions**
|     Tag    	|     Required    	|     Details    	|     Example    	|
|-	|-	|-	|-	|
|     Insight    	|     True    	|     Marks   the start of a Diagnostic XML Control    	|          	|
|     symptomId    	|     True    	|     SymptomId of the diagnostic to be   run.           	|     CannotRdpFirewall,   CannotRDPPassword          	|
|     ExecutionText    	|     False    	|     Text to   be presented to the user while the diagnostic is running.          	|     We   are running a few connectivity checks on your VM    	|
|     failedText    	|     False    	|     Text to be presented to the user   if the diagnostic fails while the diagnostic is running.    	|     We ran into   an issue and could not complete this   check          	|
|     noResultText    	|     False    	|     Text to   be presented to the user if the diagnostic successfully completes but no insight   is returned.    	|     We   have checked the current firewall configuration and did not find any issues.     	|
|     maxInsightCount    	|     False    	|     Defines the maximum number of   insights to be presented if more than one insight is returned by the   diagnostic.      If the tag is not provided the default value of 3 will be   assumed.     	|     5    	|



**Schema example:**

<insight>

     <symptomId>CannotRdpFirewall, CannotRDPPassword</symptomId> 

     <executionText>We are checking to see if your VM was restarted</executionText> 

     <timeoutText>Proceeding to the next operation</timeoutText> 

     <noResultText>No issues found. Your VM is running smoothly.</noResultText> 

</insight>

**Note**: To run each diagnostic in parallel, create separate <insight> tags each tag
   

1. **Include multiple diagnostics**
   Run multiple diagnostics in parallel by creating separate <insight> tags. For example, to give the customer a more complete picture of a resource’s state, you can include two separate insight tags from two different diagnostics. When the diagnostics finish running, insights from both diagnostics are presented to the customer. 
   With Solutions 2.0, you can place diagnostics anywhere in the article canvas, giving you complete flexibility in authoring the content to suit your customer’s needs.

**Schema example:**


### <Title>

<Diagnostic description>
<Insight> 
	<symptomId>CannotRdpFirewall</symptomId>
	<executionText>We are checking to see if your VM’s firewall settings</executionText>
	<timeoutText>Proceeding to the next operation</timeoutText>
	<noResultText>No issues found</noResultText>
</Insight>


### <Title>

<description>
<Insight>  
<symptomId>CannotRdpFirewall</symptomId>
<executionText>We are checking to see if your VM’s firewall settings</executionText>
<timeoutText>Proceeding to the next operation</timeoutText>
<noResultText>No issues found</noResultText>
</Insight> 
	

2. **Limit the number of insights per diagnostic**
   Control the number of insights that the diagnostic returns by including the <maxInsightCount> property in the <insights> tag. This property controls the number of critical insights that we showcase to the customer. In the portal, only critical insights are surfaced. In the following example, only two insights will be shown. If this property is omitted, the portal will return 3 critical insights.

**Schema example**:

### <Title>

<description>
<insight>
       <symptomId>SqlLtsFailedLogin,SqlConnectivity,SqlCustomerVerbatims,SqlLts,SqlConnectivityBasic</symptomId><br>
       <executionText>The diagnostic is running some checks on your resource</executionText><br>
      <timeoutText>This check was taking too long, so we stopped the operation</timeoutText><br>
      <noResultText>The diagnostic did not find any issues. Use the troubleshooting steps below to resolve your problem</noResultText><br>
      <additionalInputsReq>true</additionalInputsReq><br>
      <maxInsightCount>2</maxInsightCount><br>
</insight>


## Azure Monitor charts

Azure Monitor charts target several key performance indicators (KPIs) to help the customer determine how well their resource is performing.

- Provide a succinct title for the chart that corresponds to the y-axis.
- Explain what information to look for and how the reader will use that information. This text is required to ensure accessibility for all users.

**Example**:

**Resolve RBAC authorization failures in Blob Storage**

Look for spikes in the following chart to determine when and how authorization failures have occurred.

![Chart showing auth failures](../assets/images/ApolloChart.png)

**Schema example:**


### <Title>

<Metric description>
	
<metric>
     <name>Disk Write Operations/Sec</name>
     <aggregationType>Sum</aggregationType>
     <timeSpanDuration>1d</timeSpanDuration>
     <title>Virtual Machine Disk Write Operations/Sec</title>
</metric>

**Metrics schema definitions**

| Tag  	| Required  	| Details  	| Example  	|
|-	|-	|-	|-	|
| Name  	| True  	| Type of the Azure monitor metric  	|  Disk Write Operations  	|
| aggregationType  	| True  	| SymptomId of the diagnostic to be executed. Specify Sum, Avg, Count, or Percentile (default is value Sum)     	| CannotRdpFirewall, CannotRDPPassword     	|
| timeSpanDuration  	| False  	| Text to be presented to the user while the diagnostic is executing.    	| We are running a few connectivity checks on your VM  	|
| timeSpanDuration  	| False  	| Text to be presented to the user if the diagnostic fails while the diagnostic is executing. Use d for day (one day is the default) and m for minute.  	| We ran into an issue and could not complete this check    	|
| title  	| False  	| Text to be presented to the user if the diagnostic successfully completes but no insight is returned.  	| We have checked the current firewall configuration and did not find any issues.   	|

## Video solutions

Video solutions have the power to engage the customer by stimulating their senses. Video solutions allow you to walk the customer through the steps of a task and show them what the end result should look like. Video solutions can support an accompanying procedure or stand alone as a solution.
- Include a title and summary of the instructions or content in the video. Text instructions are usually easier to follow and are more accessible than pure video content.
- Apollo can accommodate a single video and groups of (up to three) smaller videos.
- When possible, call out key points of the video and where they occur in the timeline.
- Video solutions require XML tags. 

**Example:**

In the following video, you'll learn to configure Azure AD authentication and create users/logins in Azure SQL.

![Demo of Azure AD authentication for Azure SQL](../assets/images/ApolloLargeVideo.png)

Summary of configuration steps in the video:

1. Setting up an Azure Active Directory admin
2. Creating logins for users
3. Examples of login types
4. Adding access to existing AD users

**Example:**

In the following videos, you'll learn the basics of continuous integration (CI) within Azure DevOps.

![Continuous integration and build](../assets/images/ApolloSmVideo1.jpg) ![Azure DevOps tutorial](../assets/images/ApolloSmVideo2.jpg)

**Video schema examples**

- **Single video example**

### <title>

<description>
<video>
<src> https://tinyurl.com/yyt9xah2 </src>
<title> **Configure Azure AD authentication for Azure SQL, 8:56** </title>
</video>


- **Multiple videos example**

### <title>

<description>
<videoGroup>
     <video>
     <src> https://tinyurl.com/yxf42xvg </src>
     <title> **CI – CD with Azure DevOps, 13:25** </title>
     </video>
     <video>
     <src>https://www.youtube.com/watch?v=-Peb5IPGvVI</src>
     <title> **Azure DevOps tutorial explains the basics for beginners, 1:00:11** </title>
     </video>
</videoGroup>

| Tag  	| Required  	| Details  	| Example  	|
|-	|-	|-	|-	|
| videoGroup  	| False  	| Required if you have multiple videos grouped together  	|   	|
| Video  	| True  	|   	|   	|
| Src  	| True  	| Link to the video  	|  Disk Write Operations  	|
| Title  	| True  	|    	| CannotRdpFirewall, CannotRDPPassword     	|


## Images

Images are an excellent way to demonstrate and support both conceptual information and tasks in procedures. Apollo supports only web-hosted images.

- No heading required
- URLs only, no relative links
- Replace "alt text" with a concise description of what is being shown in the image (without punctuation) to ensure accessibility for all users
- For screenshots, make sure that they contain legible text
- Use colored boxes, not highlighting, to call out particular elements

**Image example**

This screenshot shows how you can back up a disk using incremental snapshots.

![Back up disks using incremental snapshots](../assets/images/ApolloImage.png)

**Image schema**

![alt text](URL)


## Tables

Use tables to make reference content more scannable. Only Markdown tables are permitted in your solution.

**Example**

![Table showing article IDs](../assets/images/ApolloTable.png)


**Example of table schema**

|No|Microsoft Cloud Germany (MCG)- source |Azure Global Cloud (AGC)- target |

|--|--|--|

|1 |a312i8348c-dd9f-442c-a531-021090a25833 |9909093ce-dd9f-442c-a531-021090a25883 |

|2 |a312i8348c-dd9f-442c-a531-021090a25833 |QX3455555e-449f-R23GB-c333-73jdj876eir0 |


# AzureKB

AzureKB is a service that ingests content from many places (Azure public docs, Stack, MSDN, Q&A, support cases from DfM, IcM incidents, etc) and returns relevant articles for Azure specific problems. On the portal side, this shows up as a set of links available to the customer (external sources only) that AzureKB believes are relevant to the problem.
- Include AzureKB schema in the **Resources** section with any links to related and recommended articles
- Keep the links to documentation short and extremely relevant to the solution
- Don't have a link farm. Solutions with lots of links typically have lower deflection rates. More than 5 links reduces the usability of the entire solution.

**Example**

**Resources**

Here are some relevant results from the web:<br>
![AzureKB portal](../assets/images/ApolloReferences.png)

**AzureKB schema example**

### **Resources**

<azureKB>portal</azureKB>

| Tag  	| Required  	| Details  	| Example  	|  	|
|-	|-	|-	|-	|-	|
| azureKB  	| True  	|   	|   	|  	|


## Procedures

One of the most helpful solutions you can provide is step-by-step instructions for resolving an identified problem.
- Level 3 heading required.
- Use Markdown to format solutions and procedures, specifically for unordered and ordered lists (see examples).
- All lists require an empty line before the first item and after the last item.

**Example of a step-by-step procedure**

Tasks that must be performed in a particular order are called _ordered lists_. In Apollo solutions, ordered lists items are preceded with a number. Nested steps always start with a Roman numeral. To format, type 1 or the sequential number before each task, as shown here.

### <title>

<description>

1. This is a step with a link to an [external article](https://)
2. This is step with no link, blade, or instructions. Note that because the next line is a continuation of the list, no <br>; (br) break is needed.
3. This step does not have multiple sentences, so no period is required at the end
4. As in the example above, this step contains multiple sentences. When a step has multiple complete sentences, the use of a period to end each sentence is acceptable.
5. This is a step with a [link to a blade](data-blade:extensionName.bladeName.nameOfInputParam.valueOfInputParam)
6. This step uses single back ticks to enclose inline code: `SELECT name, is_disabled FROM sys.sql_logins`
7. This step uses 3 back ticks before and after to enclose multiline code. Include a blank line before and after the code block. Note that inline code blocks must be indented:

   ```
   [cluster my-cluster]
   FormLayout = selectionpanel
   Category = My Templates
   CategoryOrder = 100
   MaxCount = 200
   Autoscale = $Autoscale
   ```

**Example of a non-sequential procedure (or list of disparate tasks)**

Lists of tasks that do not follow any particular order are called *unordered lists*. Unordered lists use bullets. Only two levels of bullets are supported. (For step-by-step instructions, use an ordered list.)

### <title>

<description>

* Item1
* Item2
* Item3
   * Sub-ItemA
   * Sub-ItemB

## Rules

These rules ensure that your self-help articles meet both the validation rules in Elixir and the Microsoft style guidelines. For details and examples, review the ![**Authoring guidelines**](../assets/articles/AuthoringGuidelines.md).

* At minimum, the body must contain substantive content that clearly addresses the topic or issue. For an **issue-based** solution, the body contains a solution that specifically addresses the stated issue. For a **how-to solution** , the body contains conceptual or procedural information, or both.

* Use active, imperative verbs and present tense (not passive verbs; not past or future tense)

* Use contractions ("don't"; instead of "do not"; "you'll instead of "you will")

* Use sentence capitalization for all headings (capitalize only the first word)

* Check product, feature, and service names for accuracy, including capitalization

* Spell out product, feature, and service names on first mention, followed by acronym in parentheses ("Azure Active Directory (AAD)"), and after that, use the acronym ("AAD")

* Use "select" not "click"

* Don't use "please"

* Bold all UI elements. Don't overuse bold in text.

* Use code formatting for code (inline and block), values, parameters, properties, operations, methods, functions, language keywords, and directory and file names

* Enclose error messages in text in quotation marks

* Insert a blank line after every heading

* Insert a blank line <br> before each level 3 heading 

* Tables must be created in Markdown

* Include only YouTube video URLs that don't contain an ampersand (&) 

* All non-text content (images, charts, videos) must include alt text to meet Microsoft Accessibility Standards. At minimum, include an introductory sentence that briefly describes the content. 

* Link text must clearly indicate the purpose of link ("here" or "this document" is not sufficient)

* Don't use aka.ms links or links to internal documentation ("review.microsoft.docs")
