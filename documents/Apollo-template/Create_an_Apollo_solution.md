# Create an Apollo solution

_[All phrases in red need to be linked to the relevant documents.]_

Use this document to get started constructing Apollo articles. Here, we'll describe the Apollo article structure, solution components
you can use within that structure, and the basic requirements for building a sound Apollo solution. For a complete description of 
Apollo, see the **Overview**.

## Get started

- To create a solution from scratch,[download the raw format of the Apollo template in Markdown](https://github.com/Azure/SelfHelpContent/blob/master/documents/Apollo-template/Apollo-template.md). Alternatively, you can create an Apollo solution in Elixir and simply choose the components you want in your solution (versus typing the schema).
- Include all **required** components in the order they appear. See also **Template and examples** for ideas on how to write an article.
- Format your article in Markdown, unless XML is specifically called for.
- Review the [**Rules**](#_Rules) to avoid validation warnings and errors. Rules are in place to ensure your solution meets Microsoft standards for writing style, formatting, links, and accessibility.

## Basic structure of an Apollo solution

| Section | Required? | Purpose |
| --- | --- | --- |
| **Properties** | **Yes** | Contains the metadata of the article |
| **Internal title** | **Yes** | Internal only (not customer-facing) component used by the Azure self-help portal |
| **Customer-facing title** | **Yes** | Provides context for your Apollo solution |
| **Body** | **Yes** | Main canvas of the article. **At minimum** , must contain **an**** introduction **and** one solution component:
|          |         |- Diagnostics
|          |         |- Azure Monitor charts
|          |         |- Video solutions
|          |         |- Images
|          |         |- Procedures
|          |         |- Tables
|          |         |- AzureKB article links
 |

## Properties section

The properties section is required and contains the metadata of the article. All self-help articles must start with a **properties** section. For details about property metadata, see the following topic.

- Some properties are mandatory, others are optional. However, we ask that you include all properties and assign an empty string (&quot;&quot;) as the value for properties you aren&#39;t using.
- Neither the order of the properties, spaces or capitalization matters
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

| **Tag** | **Description** | **Required** | **Notes** | **Example** |
| --- | --- | --- | --- | --- |
| pageTitle | Name of the issue for troubleshoot content | Yes | \* This will not appear on the portal, it is metadata only
 \* This can only be one sentence - do not include periods or commas | \* Database Connectivity issue due to invalid credentials detected
 \* VM boot error |
| description | Name of the issue or any other description you would like. | Yes

 | This will not appear on the portal, it is metadata only | \* IsBadPassword
 \* Virtual machine failed to boot with error code 0xc000000e |
| ms.author | Microsoft alias for the author | Yes | Microsoft alias of the person who wrote or last edited the documen | \* bernardm
\* ramakk |
| displayOrder | Not applicable to Insights | Only for articles displayed in the Help and Support blade (aka Troubleshoot blade) |
 |
 |
| articleId | Unique identifier for the article | Yes | \* MUST be unique for all Insight articles
\* We highly recommend using the file name (which by default is also unique) | \* isbadpassword \* errorcod-e0xc000000e |
| selfHelpType | Set the value to &quot;Apollo&quot; | Yes |
 |
 |
| supportTopicIds | Support Topic Ids for which this content will be presented in case submission | Only for Diagnostic articles and articles that will be presented during case submission | \* Must match a valid support topic for the Resource Provider and Resource Type
 \* Must match the support topic Id for which a Diagnostic Scenario was added in SEAM
 \* Can have multiple, comma separated values
 |
 |
| productPesIds | Product Id(s) for the service for which the article will be presented | Yes | \* Must match a valid PesId for the Resource Provider and Resource Type
 \* In the case of diagnostics articles, it must match the PesId for which a Diagnostic Scenario was added in SEAM
 \* Can have multiple, comma separated values
 | \* &quot;14749&quot;
\* &quot;14749, 15571&quot; |
| resourceRequired |
 |
 |
 |
 |
| cloudEnvironments | Indicates if the content specific to a certain cloud. Possible values: &quot;public, blackForest, fairfax and mooncake&quot; | Yes | \* Can have multiple, comma separated values | \* &quot;public&quot;
\* &quot;public, fairfax&quot; |
| ownershipId | Indicates the ownershipId who is responsible for this selfhelp asset | Yes | ­­ | ownershipId=&quot;Compute\_BotService&quot; |

## Internal title

Internal-only title **required** for internal reference. Level 1 heading. Use the following Markdown format.

**# Title**


## Customer-facing title

Required. Level 2 heading that describes the article contents, preferably in 10 words or less. The title and provides necessary
context to the customer and reassurance that the solution targets their concern. Use sentence capitalization: Capitalize only the
first word and any product, feature, or service names. Start with an active verb (such as resolve, enable, learn, troubleshoot, etc.)

**Examples:**

- "Troubleshoot High CPU Usage for your Virtual Machines"
- "Troubleshoot most commonly occurring performance issues using diagnostics and recommended document links below."
- "Learn How to Enable Auditing for your SQL DB"
- "Enable AD DS Authentication for Azure Files and Windows Virtual Desktop"

Use the following Markdown schema. Do not add **bold** formatting. Markdown headings are bolded, by default.

**## Title**


## Body section<br>
The body comes immediately after the customer-facing title and contains the _entire article contents_. Think of the body section
as your canvas where you can place any combination of content and solution components. Always start with a brief 
[introduction](#_Introduction/Issue_statement) that lets the customer know what they can expect from the solution.

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
- Azure KB and document links

The following sections describe each component and provide examples and schema for each.

## Diagnostics

Optional. Level 3 heading required. Add a blank line before the heading.<br>

Diagnostics are a feature of Azure Cloud Services that let you diagnose and collect data on the customer's deployed application. 
When you include a diagnostic in your solution, explain what it is and what information it's gathering, and how the customer
can use that information to address their issue.

**Example:**

### VM CPU performance

Review the graph to see the CPU usage as it correlates to your workload. Identify any patterns or spikes that are tied to the load, scheduled jobs, or unexpected consumption of resources.

![Graph of your workload's CPU usage](RackMultipart20210209-4-sl88e3_html_d9a4372cba82fb8c.png)

### What can cause a CPU spike on a VM?

High CPU can indicate that the application is performing many CPU-intensive tasks relative to the incoming load. This can indicate that the application is not performing as efficiently as expected or has insufficient resources to handle loads. Some common factors to high CPU include:

1. A recent code change or deployment
2. A recent patch on the OS level or accumulative patches/fixes on the Application
3. Query change or outdated Indexes. SQL or Oracle data tier applications also have query plan optimizations. Lack of proper indexes, data changes, etc. can lead to some queries becoming more compute intensive.

**Diagnostics schema definitions**

| **Tag** | **Required** | **Details** | **Example** |
| --- | --- | --- | --- |
| **Insight** | True | Marks the start of a Diagnostic XML Control | |
| **symptomId** | True | SymptomId of the diagnostic to be run.
 | CannotRdpFirewall, CannotRDPPassword |
| **ExecutionText** | False | Text to be presented to the user while the diagnostic is running.
 | We are running a few connectivity checks on your VM |
| **failedText** | False | Text to be presented to the user if the diagnostic fails while the diagnostic is running. | We ran into an issue and could not complete this check
 |
| **noResultText** | False | Text to be presented to the user if the diagnostic successfully completes but no insight is returned. | We have checked the current firewall configuration and did not find any issues. |
| **maxInsightCount** | False | Defines the maximum number of insights to be presented if more than one insight is returned by the diagnostic. If the tag is not provided the default value of 3 will be assumed. | 5 |

1. **List diagnostics in \&lt;SymptomIds\&gt;**

Provide a comma-separated list of SymptomIds for the diagnostics to be run. The order in which the SymptomIds are listed matters. Azure porta prioritizes the presented results for the first diagnostic mapped to the first SymptomId. If no insight is found or the first diagnostic failed/timed-out, the portal will proceed to get the insight from the second diagnostic and so on.

**Schema example:**

<Insight>

\&lt;symptomId\&gt;CannotRdpFirewall, CannotRDPPassword\&lt;/symptomId\&gt;\&lt;br\&gt;

\&lt;executionText\&gt;We are checking to see if your VM was restarted\&lt;/executionText\&gt;\&lt;br\&gt;

\&lt;timeoutText\&gt;Proceeding to the next operation\&lt;/timeoutText\&gt;\&lt;br\&gt;

\&lt;noResultText\&gt;No issues found. Your VM is running smoothly. \&lt;/noResultText\&gt;\&lt;br\&gt;

\&lt;/Insight\&gt;

**Note** : To run each diagnostic in parallel, create separate \&lt;Insight\&gt; tags each tag

1. **Run multiple diagnostics in parallel**

If you need to run multiple diagnostics in parallel, create two separate \&lt;Insight\&gt; tags. For example, if you need to present insights from two different diagnostics for the customer to have a complete picture of a resource&#39;s state, you&#39;ll need diagnostics that check that resource for 2 different things simultaneously to provide insights from both diagnostics.

**Schema example:**

\&lt;blank line before head3s\&gt;

**### \&lt;** Title\&gt;

\&lt;Diagnostic description\&gt;

\&lt;Insight\&gt;

\&lt;symptomId\&gt;CannotRDPPassword\&lt;/symptomId\&gt;\&lt;br\&gt;

\&lt;executionText\&gt;We are checking to see if your VM was restarted\&lt;/executionText\&gt;\&lt;br\&gt;

\&lt;timeoutText\&gt;Proceeding to the next operation\&lt;/timeoutText\&gt;\&lt;br\&gt;

\&lt;noResultText\&gt;No issues found. Your VM is running smoothly.\&lt;/noResultText\&gt;\&lt;br\&gt;

\&lt;/Insight\&gt;

\&lt;blank line before head3s\&gt;

**###** \&lt;Title\&gt;

\&lt;Diagnostic description\&gt;

\&lt;Insight\&gt;

\&lt;symptomId\&gt;CannotRdpFirewall,\&lt;/symptomId\&gt;\&lt;br\&gt;

\&lt;executionText\&gt;We are checking to see if your VM was restarted\&lt;/executionText\&gt;\&lt;br\&gt;

\&lt;timeoutText\&gt;Proceeding to the next operation\&lt;/timeoutText\&gt;\&lt;br\&gt;

\&lt;noResultText\&gt;No issues found. Your VM is running smoothly.\&lt;/noResultText\&gt;\&lt;br\&gt;

\&lt;/Insight\&gt;

1. **Present multiple insights per diagnostic in \&lt;maxInsightCount\&gt;**

Control the number of insights that the diagnostic returns using the \&lt;maxInsightCount\&gt; property inside the \&lt;Insights\&gt; tag. This property controls the number of critical insights that we showcase to the customer. In the portal, only critical insights are surfaced. In the following example, the insights are limited to two.

If this property is not defined, then we return three critical insights.

**Example** :

\&lt;blank line before head3s\&gt;

**###** \&lt;Title\&gt;

\&lt;Diagnostic description\&gt;

\&lt;Insight\&gt;

\&lt;symptomId\&gt;SqlLtsFailedLogin,SqlConnectivity,SqlCustomerVerbatims,SqlLts,SqlConnectivityBasic\&lt;/symptomId\&gt;

\&lt;executionText\&gt;The diagnostic is running some checks on your resource\&lt;/executionText\&gt;

\&lt;timeoutText\&gt;This check was taking too long, so we stopped the operation\&lt;/timeoutText\&gt;

\&lt;noResultText\&gt;The diagnostic did not find any issues. Use the troubleshooting steps below to resolve your problem\&lt;/noResultText\&gt;

\&lt;additionalInputsReq\&gt;true\&lt;/additionalInputsReq\&gt;

\&lt;maxInsightCount\&gt;2\&lt;/maxInsightCount\&gt;

\&lt;/Insight\&gt;

# Azure Monitor charts

Azure Monitor charts target several key performance indicators (KPIs) to help the customer determine how well their resource is performing.

- Provide a succinct title for the chart that corresponds to the y-axis.
- Explain what information to look for and how the reader will use that information. This text is required to ensure accessibility for all users.

**Example** :

**Resolve RBAC authorization failures in Blob Storage**

Look for spikes in the following chart to determine when and how authorization failures have occurred.

![](RackMultipart20210209-4-sl88e3_html_88e560f6a7bd374e.png)

**Schema example:**

\&lt;blank line before head3s\&gt;

**###** \&lt;Title\&gt;

\&lt;Metric description\&gt;

\&lt;metric\&gt;

\&lt;name\&gt;Disk Write Operations/Sec\&lt;/name\&gt;

\&lt;aggregationType\&gt;Sum\&lt;/aggregationType\&gt;

\&lt;timeSpanDuration\&gt;1d\&lt;/timeSpanDuration\&gt;

\&lt;title\&gt;Virtual Machine Disk Write Operations/Sec\&lt;/title\&gt;

\&lt;/metric\&gt;

**Metrics schema definitions**

| **Tag** | **Required** | **Details** | **Example** |
| --- | --- | --- | --- |
| **Name** | True | Type of the Azure monitor metric | Disk Write Operations |
| **aggregationType** | True | SymptomId of the diagnostic to be executed. Specify Sum, Avg, Count, or Percentile (default is value Sum) | CannotRdpFirewall, CannotRDPPassword |
| **timeSpanDuration** | False | Text to be presented to the user while the diagnostic is executing.
 | We are running a few connectivity checks on your VM |
| **timeSpanDuration** | False | Text to be presented to the user if the diagnostic fails while the diagnostic is executing. Use d for day (one day is the default) and m for minute. | We ran into an issue and could not complete this check
 |
| **title** | False | Text to be presented to the user if the diagnostic successfully completes but no insight is returned. | We have checked the current firewall configuration and did not find any issues. |

# Video solutions

Video solutions have the power to engage the customer by stimulating their senses. Video solutions allow you to walk the customer through the steps of a task and show them what the end result should look like. Video solutions can support an accompanying procedure or stand alone as a solution.

- Optional
- Level 3 heading
- Include a title and summary of the instructions or content in the video. Text instructions are usually easier to follow and are more accessible than pure video content.
- Apollo can accommodate a single video and groups of 2-3 smaller videos.
- When possible, call out key points of the video and where they occur in the timeline.

**Example (single video):**

In the following video, you&#39;ll learn to configure Azure AD authentication and create users/logins in Azure SQL.

![](RackMultipart20210209-4-sl88e3_html_a4d354aba88f5def.png)

Summary of configuration steps in the video:

1. Setting up an Azure Active Directory admin
2. Creating logins for users
3. Examples of login types
4. Adding access to existing AD users

**Multiple video example:**

In the following videos, you&#39;ll learn the basics of continuous integration (CI) within Azure DevOps.

![](RackMultipart20210209-4-sl88e3_html_4ef55c97b93402f5.jpg) ![](RackMultipart20210209-4-sl88e3_html_faccda19c3fb30e8.jpg)

**Video schema examples**

Video solutions require XML tags. **Important:** Make sure that the URL in the \&lt;src\&gt; tag doesn&#39;t contain ampersands (&amp;) as these will generate validation errors.

- **Single video example**

### \&lt;title\&gt;

\&lt;description\&gt;

\&lt;video\&gt;

\&lt;src\&gt; https://tinyurl.com/yyt9xah2 \&lt;/src\&gt;

\&lt;title\&gt; **Configure Azure AD authentication for Azure SQL, 8:56** \&lt;/title\&gt;

\&lt;/video\&gt;

- **Multiple videos example**

### \&lt;title\&gt;

\&lt;description\&gt;

\&lt;videoGroup\&gt;

\&lt;video\&gt;

\&lt;src\&gt; https://tinyurl.com/yxf42xvg \&lt;/src\&gt;

\&lt;title\&gt; **CI – CD with Azure DevOps, 13:25** \&lt;/title\&gt;

\&lt;/video\&gt;

\&lt;video\&gt;

\&lt;src\&gt;https://www.youtube.com/watch?v=-Peb5IPGvVI\&lt;/src\&gt;

\&lt;title\&gt; **Azure DevOps tutorial explains the basics for beginners, 1:00:11** \&lt;/title\&gt;

\&lt;/video\&gt;

\&lt;/videoGroup\&gt;

| **Tag** | **Required** | **Details** | **Example** |
| --- | --- | --- | --- |
| **videoGroup** | False | Required if you have multiple videos grouped together |
 |
| **Video** | True |
 |
 |
| **Src** | True | Link to the video | Disk Write Operations |
| **Title** | True | | CannotRdpFirewall, CannotRDPPassword |

# Images

Images are an excellent way to demonstrate and support both conceptual information and tasks in procedures. Apollo supports only web hosted images.

- Optional
- No heading is required
- Replace &quot;alt text&quot; with a concise description of what is being shown in the image (without punctuation) to ensure accessibility for all users

- For screenshots, make sure that they contain legible text
- Use colored boxes, not highlighting, to call out particular elements

**Image example**

This screenshot shows how you can back up a disk using incremental snapshots.

![](RackMultipart20210209-4-sl88e3_html_5a02e9665c6faf18.png)

**Image schema**

![alt text](/images/image.png)

[Back up your disk using incremental snapshots](../windows/media/incremental-snapshots/storage-incremental-snapshots-1.png)

#

# Tables

Use tables to make reference content more scannable. Only Markdown tables are permitted in your solution.

**Example**

![](RackMultipart20210209-4-sl88e3_html_181b756cc63908a.png)

**Table schema**

|No|Microsoft Cloud Germany (MCG)- source |Azure Global Cloud (AGC)- target |

|--|--|--|

|1 |a312i8348c-dd9f-442c-a531-021090a25833 |9909093ce-dd9f-442c-a531-021090a25883 |

|2 |a312i8348c-dd9f-442c-a531-021090a25833 |QX3455555e-449f-R23GB-c333-73jdj876eir0 |

# AzureKB

AzureKB is a service that ingests content from many places (Azure public docs, Stack, MSDN, Q&amp;A, support cases from DfM, IcM incidents, etc) and returns relevant articles for Azure specific problems. On the portal side – this shows up as a set of links available to the customer (external sources only) that AzureKB believes are relevant to the problem.

- Include AzureKB schema in the **Resources** section with any links to related and recommended articles
- Keep the links to documentation short and extremely relevant to the solution
- Don&#39;t have a link farm. Solutions with lots of links typically have lower deflection rates. More than 5 links reduces the usability of the entire solution.

**Example**

**Resources**

Here are some relevant results from the web: ![](RackMultipart20210209-4-sl88e3_html_5d88f0cd263f7607.png)

**AzureKB schema example**

### **Resources**

\&lt;introduction\&gt;

\&lt;azureKB\&gt; \&lt;/azureKB\&gt;

**Note** : To include the azureKB portal in the **Resources** section, use this schema:
 \&lt;azureKB\&gt;portal\&lt;/azureKB\&gt;

| **Tag** | **Required** | **Details** | **Example** |
| --- | --- | --- | --- |
| **azureKB** | True |
 |
 |

# Procedures

One of the most helpful solutions you can provide is step-by-step instructions for resolving an identified problem.

-
- Level 3 heading required.
- Use Markdown to format solutions and procedures, specifically for unordered and ordered lists (see examples).
- All lists require an empty line before the first item and after the last item.

**Example of a step-by-step procedure**

Tasks that must be performed in a particular order are called _ordered lists_. In Apollo solutions, ordered lists items are preceded with a number. Nested steps always start with a Roman numeral. To format, type 1 or the sequential number before each task, as shown here.

### \&lt;title\&gt;

\&lt;description\&gt;

1. This is a step with a link to an [external article](https://)
2. This is step with no link, blade, or instructions. Note that because the next line is a continuation of the list, no \&lt;br\&gt; (br) break is needed.
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

Lists of tasks that do not follow any particular order are called _ **unordered lists** _. Unordered lists use bullets. Only two levels of bullets are supported. (For step-by-step instructions, use an ordered list.)

### \&lt;title\&gt;

\&lt;description\&gt;

\* Item1

\* Item2

\* Item3

\* Sub-ItemA

\* Sub-ItemB

# Rules

These rules ensure that your self-help articles meet both the validation rules in Elixir and the Microsoft style guidelines. For details and examples, review the **Authoring guidelines**.

\* At minimum, the body must contain substantive content that clearly addresses the topic or issue. For an **issue-based** solution, the body contains a solution that specifically addresses the stated issue. For a **how-to solution** , the body contains conceptual or procedural information, or both.

\* Use active, imperative verbs and present tense (not passive verbs; not past or future tense)

\* Use contractions (&quot;don&#39;t&quot; instead of &quot;do not&quot;; &quot;you&#39;ll&quot; instead of &quot;you will&quot;)

\* Use sentence capitalization for all headings (capitalize only the first word)

\* Check product, feature, and service names for accuracy, including capitalization

\* Spell out product, feature, and service names on first mention, followed by acronym in parentheses (&quot;Azure Active Directory (AAD)&quot;), and after that, use the acronym (&quot;AAD&quot;)

\* Use &quot;select,&quot; not &quot;click&quot;

\* Don&#39;t use &quot;please&quot;

\* Bold all UI elements. Don&#39;t overuse bold in text.

\* Use code formatting for code (inline and block), values, parameters, properties, operations, methods, functions, language keywords, and directory and file names

\* Enclose error messages in text in quotation marks

\* Insert a blank line after every heading

\* Insert a blank line \&lt;br\&gt; before each level 3 heading \&lt;h3\&gt; **- We should fix**

\* Tables must be created in Markdown

\* Include only YouTube video URLs that don&#39;t contain an ampersand (&amp;) **– We should fix this.**

\* All non-text content (images, charts, videos) must include alt text to meet Microsoft Accessibility Standards. At minimum, include an introductory sentence that briefly describes the content. – **blocking**

\* Link text must clearly indicate the purpose of link (&quot;here&quot; or &quot;this document&quot; is not sufficient)

\* Don&#39;t use aka.ms links or links to internal documentation (&quot;review.microsoft.docs&quot;)

_[__**Editorial note [JR]**__: We can sort the Rules by priority or category (style, formatting, accessibility, etc.); I think category would be the most useful. Additionally, after we determine which rules can be nonblocking validation rules, we&#39;ll call those out separately, with a brief explanation that if the article doesn&#39;t follow those rules, the author will see a nonblocking comment and can make that correction before submitting the PR for review. This will expedite the review process.]_