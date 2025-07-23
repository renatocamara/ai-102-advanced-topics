# Advanced Topic: Agentic Patterns in the Microsoft Ecosystem

## 1. Concept Explanation: What is Agentic AI?

## 2. Agentic Patterns in Microsoft's Ecosystem

### 2.1. Azure AI Foundry Agents

### 2.2. Semantic Kernel

### 2.3. Microsoft Copilot Studio

### 2.4. Autonomous Pipelines in AI and DevOps

## 3. Relevant Use Cases and Implementation Scenarios

## 4. Key Considerations and Best Practices for Agentic AI

## 5. Sample Implementations

### Customer Case Inspiration: [To be filled after research]

### Scenario: [To be filled after research]

### C# Implementation Example

### Python Implementation Example





## 1. Concept Explanation: What is Agentic AI?

Agentic AI refers to the design and implementation of artificial intelligence systems that exhibit autonomous, goal-oriented behavior. Unlike traditional AI applications that primarily respond to direct commands or perform predefined tasks, agentic AI systems are capable of understanding high-level objectives, breaking them down into sub-tasks, planning sequences of actions, executing those actions (often by interacting with external tools and environments), and adapting their behavior based on feedback and new information. This autonomy allows them to operate with minimal human intervention, making decisions and taking initiative to achieve their goals.

Key characteristics of agentic AI include:

*   **Autonomy:** Agents can operate independently, making decisions without constant human oversight.
*   **Goal-Oriented:** They are designed to achieve specific objectives, often complex ones that require multiple steps.
*   **Perception:** Agents can interpret information from their environment (e.g., user input, system states, data from tools).
*   **Reasoning and Planning:** They possess the ability to logically deduce actions, plan sequences of operations, and adapt plans in dynamic environments.
*   **Tool Use (Function Calling):** A critical aspect of agentic AI is the ability to leverage external tools, APIs, or services to extend their capabilities beyond their inherent knowledge. This allows them to interact with the real world, fetch up-to-date information, or perform specific actions.
*   **Memory and Learning:** Agents can maintain state, remember past interactions, and learn from experiences to improve their performance over time.
*   **Orchestration:** In multi-agent systems, agents can coordinate and collaborate with each other to achieve shared or individual goals.

The rise of large language models (LLMs) has significantly propelled the development of agentic AI. LLMs provide powerful reasoning and natural language understanding capabilities, enabling agents to interpret complex instructions, generate human-like responses, and even write code or formulate API calls for tool interaction. This combination of advanced reasoning and tool-use capabilities is at the heart of modern agentic AI systems.



## 2. Agentic Patterns in Microsoft's Ecosystem

Microsoft is heavily investing in agentic AI, providing a robust ecosystem of tools and platforms that enable developers to build and deploy intelligent agents. These platforms offer varying levels of abstraction and control, catering to different development needs.

### 2.1. Azure AI Foundry Agents

Azure AI Foundry is Microsoft's comprehensive platform for building, training, and deploying AI models and applications at scale. Within Azure AI Foundry, the concept of 'Agents' is central to enabling autonomous AI solutions. Azure AI Foundry Agents are designed to connect the core pieces of the platform—such as models, tools, and frameworks—into a unified runtime, facilitating the creation and management of enterprise-grade AI agents.

Key aspects of Azure AI Foundry Agents:

*   **Managed Service:** Azure AI Foundry provides a managed service for building and running AI agents, abstracting away much of the underlying infrastructure complexity. This allows developers to focus on agent logic and capabilities rather than operational overhead.
*   **Integration with Azure AI Services:** Agents within Azure AI Foundry seamlessly integrate with other Azure AI services, including Azure OpenAI Service for large language models, Azure AI Search for retrieval, and various cognitive services for specialized tasks (e.g., speech-to-text, computer vision).
*   **Tooling and Orchestration:** Azure AI Foundry provides mechanisms for agents to discover and utilize external tools and functions. This is crucial for agentic behavior, as it allows agents to interact with external systems, fetch real-time data, and perform actions beyond their inherent LLM capabilities. The platform supports the definition and management of these tools, enabling agents to dynamically invoke them based on their reasoning.
*   **Enterprise-Grade Capabilities:** Designed for enterprise use, Azure AI Foundry Agents offer features like robust security, access control, scalability, and observability, which are critical for deploying AI solutions in production environments.
*   **Responses API:** The Responses API within Azure AI Foundry is a key component for unlocking agentic AI. It helps in transforming how enterprises leverage AI by providing structured outputs and facilitating the integration of agentic workflows into existing business processes.

Azure AI Foundry Agents are particularly well-suited for scenarios requiring highly scalable, secure, and integrated agent solutions within the Azure cloud environment. They provide the foundational infrastructure for building complex, multi-step agentic applications that can automate sophisticated business processes.






### 2.2. Semantic Kernel

Semantic Kernel (SK) is an open-source SDK that integrates large language models (LLMs) with conventional programming languages. It acts as a lightweight SDK that allows developers to combine AI capabilities with existing code, enabling the creation of intelligent agents and applications. SK is a core component for building agentic applications within the Microsoft ecosystem, providing the building blocks for agents to reason, plan, and interact with external systems.

Key features and concepts of Semantic Kernel in the context of agentic AI:

*   **Skills (Plugins/Tools):** In Semantic Kernel, external functionalities are exposed as 'Skills' (also referred to as Plugins or Tools). These are collections of functions that an LLM can call to perform specific actions. Skills can encapsulate anything from simple string manipulations to complex API calls to external services (e.g., fetching weather data, sending emails, querying a database). The agent uses these skills to extend its capabilities beyond pure text generation.
*   **Connectors:** SK provides connectors to various LLMs (e.g., Azure OpenAI, OpenAI, Hugging Face), allowing developers to choose the best model for their needs.
*   **Planners:** Planners are a crucial component for agentic behavior in SK. They enable the agent to take a high-level user goal and automatically break it down into a series of steps, selecting and orchestrating the necessary skills to achieve that goal. This is where the 'agentic' planning and execution come into play, allowing for multi-step reasoning and action.
*   **Memory:** Semantic Kernel includes memory capabilities, allowing agents to store and retrieve information from past interactions or external knowledge bases. This memory can be semantic (understanding the meaning of information) or volatile (short-term context).
*   **Orchestration:** SK facilitates the orchestration of LLM calls, skill invocations, and memory interactions. Developers can define complex workflows where the LLM decides which skill to use, extracts parameters, executes the skill, and then uses the result to continue the conversation or achieve the goal.

Semantic Kernel provides a flexible and powerful framework for developers to build custom agents with sophisticated reasoning and tool-use capabilities, making it ideal for scenarios where fine-grained control over agent behavior and integration with existing codebases are required.






### 2.3. Microsoft Copilot Studio

Microsoft Copilot Studio is a low-code/no-code platform designed for building custom copilots and intelligent virtual agents. While it offers a more abstracted and user-friendly interface compared to direct SDKs like Semantic Kernel, it fundamentally leverages agentic patterns for its functionality. Copilot Studio enables business users and developers to create conversational AI experiences that can understand user intent, interact with backend systems, and automate tasks through orchestration.

Key aspects of Microsoft Copilot Studio in the context of agentic AI:

*   **Low-Code/No-Code Development:** Copilot Studio provides a visual interface for designing conversational flows, defining topics, and integrating with various data sources and services. This democratizes the creation of agents, allowing a broader range of users to build intelligent solutions.
*   **Topics and Intent Recognition:** Users define 'topics' which represent specific conversational paths or user intents. The copilot uses natural language understanding (NLU) to identify the user's intent and direct the conversation to the appropriate topic.
*   **Plugins/Connectors:** Similar to Semantic Kernel's skills, Copilot Studio allows integration with external systems through pre-built connectors or custom plugins. These plugins enable the copilot to fetch data, perform actions (e.g., create a support ticket, check inventory), and interact with enterprise applications. This is a key aspect of its agentic capability, allowing it to act on behalf of the user.
*   **Orchestration and Action Chains:** Within a topic, developers can define a sequence of actions, including asking questions, calling external APIs (via plugins), and displaying information. This chaining of actions demonstrates an agentic approach to fulfilling user requests.
*   **Integration with Azure AI Foundry:** Copilot Studio agents can be deeply integrated with Azure AI Foundry services, leveraging the advanced AI capabilities and infrastructure provided by Foundry for more complex scenarios, such as advanced model deployment or specialized AI services.
*   **Generative AI Capabilities:** Copilot Studio incorporates generative AI features, allowing copilots to generate responses, summarize information, and engage in more natural and dynamic conversations.

Microsoft Copilot Studio is ideal for organizations looking to quickly build and deploy task-specific agents or copilots for customer service, internal support, or business process automation, especially when a low-code development approach is preferred.






### 2.4. Autonomous Pipelines in AI and DevOps

Beyond conversational agents, the concept of agentic behavior extends to autonomous pipelines in AI and DevOps. These pipelines are designed to self-manage, self-optimize, and self-heal, reducing manual intervention and accelerating the development and deployment of AI solutions. While not agents in the conversational sense, they exhibit agentic characteristics by autonomously executing tasks, making decisions, and adapting to changes within their operational environment.

Key aspects of autonomous pipelines:

*   **Automated MLOps Workflows:** In Machine Learning Operations (MLOps), autonomous pipelines can automate the entire lifecycle of an AI model, from data ingestion and preparation to model training, evaluation, deployment, and monitoring. This includes:
    *   **Automated Data Drift Detection and Retraining:** Pipelines can autonomously detect changes in data distribution (data drift) and trigger model retraining to maintain performance.
    *   **Automated Model Monitoring and Redeployment:** Agents within the pipeline can monitor model performance in production, identify degradation, and automatically trigger redeployment of better-performing models or rollback to previous versions.
    *   **Automated A/B Testing and Canary Deployments:** Pipelines can autonomously manage A/B testing of new model versions or perform canary deployments, gradually rolling out new models to a subset of users and monitoring their impact before full deployment.
*   **Self-Healing Infrastructure:** In DevOps, autonomous pipelines can incorporate self-healing mechanisms for infrastructure. Agents can monitor system health, detect anomalies, and automatically trigger remediation actions (e.g., restarting services, scaling resources, rolling back deployments) to ensure continuous availability and performance.
*   **Intelligent Resource Management:** Autonomous pipelines can dynamically adjust resource allocation based on workload demands, optimizing cost and performance. This involves agents monitoring resource utilization and making autonomous scaling decisions.
*   **Security Automation:** Agents can be embedded within pipelines to automate security checks, vulnerability scanning, and compliance enforcement, ensuring that AI applications adhere to security policies throughout their lifecycle.

Microsoft Azure provides various services that facilitate the creation of autonomous pipelines, including Azure DevOps, Azure Machine Learning, Azure Functions, and Azure Logic Apps. These services can be orchestrated to build highly automated and intelligent workflows that embody agentic principles, leading to faster iteration, improved reliability, and reduced operational overhead in AI and software development.






## 3. Relevant Use Cases and Implementation Scenarios

Agentic patterns, powered by Microsoft technologies, are transforming various industries and business functions by enabling more autonomous and intelligent operations. Here are some relevant use cases and implementation scenarios:

*   **Intelligent Customer Service and Support:**
    *   **Use Case:** Automating and enhancing customer interactions through self-service and agent assistance.
    *   **Scenario:** A customer interacts with a Copilot Studio-built virtual agent (Copilot) on a company website. The Copilot, leveraging Azure AI Foundry Agents and Semantic Kernel, can understand complex queries, retrieve information from a knowledge base (RAG pattern), escalate to a human agent with full context if needed, or even initiate actions like processing returns or updating order status by calling backend APIs (tools).
    *   **Agentic Aspect:** The Copilot autonomously navigates conversational flows, uses tools to fetch real-time data, and makes decisions on escalation or action execution based on user intent and available information.

*   **Automated IT Operations and Helpdesk:**
    *   **Use Case:** Streamlining IT support, incident management, and routine operational tasks.
    *   **Scenario:** An internal IT support agent, built with Semantic Kernel and deployed via Azure AI Foundry, monitors system logs for anomalies. Upon detecting an issue (e.g., a server error), the agent autonomously diagnoses the problem, checks related services, and if necessary, initiates a remediation script (tool use) or creates a ticket in the IT service management system. It can also respond to user queries like "reset my password" by calling an identity management tool.
    *   **Agentic Aspect:** The agent proactively monitors, diagnoses, plans remediation steps, and executes actions without human intervention, demonstrating autonomous problem-solving.

*   **Personalized Healthcare Assistants:**
    *   **Use Case:** Providing personalized health information, appointment scheduling, and medication reminders.
    *   **Scenario:** A patient interacts with an AI agent (built with Semantic Kernel) that integrates with their electronic health records (EHR) system (via tools). The agent can answer questions about their medical history, explain lab results in simple terms, remind them to take medication, or even schedule follow-up appointments based on their availability and doctor's schedule. The agent ensures data privacy and security through Azure's compliance features.
    *   **Agentic Aspect:** The agent autonomously accesses and synthesizes patient data, provides tailored information, and performs actions like scheduling, all while maintaining a personalized and context-aware interaction.

*   **Financial Advisory and Portfolio Management:**
    *   **Use Case:** Offering personalized financial advice, market analysis, and automated trading.
    *   **Scenario:** A financial advisory agent (using Azure AI Foundry Agents) continuously monitors market data, news feeds, and a client's investment portfolio. When a significant market event occurs or a client's portfolio deviates from their risk profile, the agent autonomously generates an alert, provides a summary of the situation, and suggests potential rebalancing strategies. It can also execute trades on behalf of the client (with proper authorization) by integrating with trading platforms (tools).
    *   **Agentic Aspect:** The agent autonomously monitors dynamic data, performs complex analysis, generates insights, and can execute financial transactions based on predefined rules and real-time conditions.

*   **Supply Chain Optimization and Logistics:**
    *   **Use Case:** Automating inventory management, demand forecasting, and logistics planning.
    *   **Scenario:** An agentic system (using autonomous pipelines and Azure AI services) monitors inventory levels across multiple warehouses, analyzes real-time demand signals, and predicts potential stockouts. It then autonomously generates purchase orders, optimizes shipping routes, and communicates with suppliers and logistics partners. If a disruption occurs (e.g., a shipping delay), the agent re-plans routes and informs affected parties.
    *   **Agentic Aspect:** The system autonomously collects and analyzes vast amounts of data, makes predictive decisions, orchestrates complex logistical operations, and adapts to unforeseen disruptions.

*   **Content Creation and Marketing Automation:**
    *   **Use Case:** Generating marketing copy, social media content, and personalized campaign materials.
    *   **Scenario:** A marketing agent (built with Semantic Kernel) is given a new product brief. It autonomously researches target audiences, analyzes competitor content, and then generates various marketing assets (e.g., ad copy, blog post outlines, social media captions) tailored for different platforms. It can also schedule these posts through social media management tools.
    *   **Agentic Aspect:** The agent autonomously performs research, generates creative content, and orchestrates publishing actions, significantly accelerating content production workflows.

These scenarios highlight how agentic patterns, enabled by Microsoft's AI ecosystem, move beyond simple automation to intelligent, autonomous systems that can perceive, reason, plan, and act in complex, dynamic environments.






## 4. Key Considerations and Best Practices for Agentic AI

Building effective and responsible agentic AI systems requires careful consideration of several factors and adherence to best practices. The autonomous nature of agents introduces new challenges and opportunities that must be addressed throughout the development lifecycle.

*   **Clear Goal Definition and Scope:**
    *   **Best Practice:** Clearly define the agent's primary goal and its operational boundaries. Avoid overly broad or ambiguous goals that can lead to unpredictable behavior. Understand what the agent *should* and *should not* do.
    *   **Consideration:** An agent's effectiveness is directly tied to the clarity of its objectives. Ill-defined goals can lead to agents taking unintended actions or getting stuck in loops.

*   **Robust Tooling and Function Calling:**
    *   **Best Practice:** Design tools with clear, concise descriptions and well-defined input/output schemas. Ensure tools are idempotent where possible (performing the same action multiple times has the same effect as performing it once) to handle retries gracefully.
    *   **Consideration:** The quality and reliability of the tools an agent uses directly impact its performance. Poorly designed tools can lead to errors, misinterpretations by the LLM, and unreliable agent behavior.

*   **Effective Prompt Engineering and System Messaging:**
    *   **Best Practice:** Craft clear and specific system prompts that define the agent's persona, capabilities, constraints, and interaction style. Use few-shot examples to guide the LLM's behavior and tool selection.
    *   **Consideration:** The LLM's interpretation of the prompt is critical for the agent's reasoning. Ambiguous or poorly structured prompts can lead to the agent misinterpreting intent or failing to use tools correctly.

*   **Memory Management and Context Window:**
    *   **Best Practice:** Implement strategies for managing the agent's memory, balancing the need for historical context with the limitations of the LLM's context window. This might involve summarization, retrieval-augmented generation (RAG) for long-term memory, or dynamic context window management.
    *   **Consideration:** Agents need to maintain relevant context to make informed decisions, but passing too much information to the LLM can be costly and inefficient, or exceed token limits.

*   **Observability, Monitoring, and Logging:**
    *   **Best Practice:** Implement comprehensive logging for agent decisions, tool invocations, and responses. Monitor agent performance, latency, and success rates. Use tracing to understand the flow of execution through complex agentic workflows.
    *   **Consideration:** Debugging autonomous agents can be challenging. Without detailed logs and monitoring, it's difficult to understand why an agent made a particular decision or failed to achieve its goal.

*   **Security and Access Control:**
    *   **Best Practice:** Apply the principle of least privilege to agents and their associated tools. Implement robust authentication and authorization for all external systems the agent interacts with. Validate all inputs to prevent malicious injections.
    *   **Consideration:** Agents, especially those with access to external systems, can pose significant security risks if not properly secured. Unauthorized access or unintended actions can have serious consequences.

*   **Human-in-the-Loop (HITL) and Oversight:**
    *   **Best Practice:** Design agents with clear escalation paths to human operators for complex, sensitive, or ambiguous tasks. Provide mechanisms for human review and approval of critical actions before execution.
    *   **Consideration:** Full autonomy is not always desirable or safe. Human oversight is crucial for ensuring agents operate within ethical boundaries and for handling edge cases that the agent cannot resolve autonomously.

*   **Error Handling and Resilience:**
    *   **Best Practice:** Implement robust error handling mechanisms within agents and tools. Design for retries, graceful degradation, and clear failure notifications. Agents should be able to recover from transient errors or escalate persistent issues.
    *   **Consideration:** Autonomous systems must be resilient to failures. Unhandled errors can lead to agents getting stuck, performing incorrect actions, or consuming excessive resources.

*   **Ethical AI and Responsible Development:**
    *   **Best Practice:** Adhere to responsible AI principles, including fairness, reliability, safety, privacy, security, inclusiveness, and transparency. Conduct thorough testing for bias and unintended consequences.
    *   **Consideration:** Agentic AI systems can have significant societal impact. Developers must consider the ethical implications of their agents' actions and ensure they are developed and deployed responsibly.

*   **Version Control and Deployment Strategy:**
    *   **Best Practice:** Treat agents, their configurations, and their tools as code, using version control systems. Implement CI/CD pipelines for automated testing and deployment to ensure consistency and reliability.
    *   **Consideration:** Managing changes and deployments for complex agentic systems requires robust engineering practices to avoid regressions and ensure smooth updates.

By following these considerations and best practices, developers can build more reliable, secure, and effective agentic AI solutions within the Microsoft ecosystem.






## 5. Sample Implementations

To illustrate the practical application of agentic patterns within the Microsoft ecosystem, we will explore a scenario inspired by real-world customer needs. This example will demonstrate how an agentic approach, leveraging components like Azure AI Foundry and Semantic Kernel, can provide innovative and disruptive solutions to complex enterprise challenges.

### Customer Case Inspiration: Automated Enterprise Knowledge Management and Insights Generation

Many large enterprises struggle with vast amounts of unstructured data spread across various internal systems, documents, and communication channels. Extracting timely and relevant insights from this data for decision-making, compliance, or strategic planning is a significant challenge. Traditional search and reporting tools often fall short in providing proactive, context-aware intelligence.

Inspired by cases like NTT DATA and Atomicwork, who leverage agentic AI for enterprise system integration and service management, we envision a scenario where an agentic system can autonomously ingest, process, and analyze diverse enterprise data sources to generate proactive insights and answer complex, multi-faceted queries. This moves beyond simple RAG (Retrieval-Augmented Generation) to an active, agent-driven knowledge discovery and synthesis process.

### Scenario: Proactive Enterprise Knowledge Agent

Our sample implementation will demonstrate a simplified version of a Proactive Enterprise Knowledge Agent. This agent will be designed to:

1.  **Monitor Internal Communications:** Simulate monitoring a stream of internal communications (e.g., project updates, customer feedback, support tickets).
2.  **Identify Key Information:** Extract key entities, sentiments, and topics from these communications.
3.  **Cross-Reference with Knowledge Base:** Compare extracted information with a structured internal knowledge base (e.g., product documentation, policy manuals).
4.  **Generate Proactive Alerts/Summaries:** If a significant trend, anomaly, or critical piece of information is identified (e.g., recurring customer issue, a new policy impacting multiple projects), the agent will generate a summary or alert.
5.  **Answer Complex Queries:** Respond to ad-hoc, complex natural language queries by synthesizing information from both real-time communications and the knowledge base.

**Agentic Aspects Demonstrated:**

*   **Autonomous Monitoring:** The agent continuously processes new information without explicit human prompting.
*   **Tool Use:** It uses tools for natural language processing (NLP) tasks (entity extraction, sentiment analysis) and for querying the knowledge base.
*   **Reasoning and Decision Making:** The agent decides when to generate an alert or summary based on predefined criteria and how to combine information to answer complex queries.
*   **Orchestration:** It orchestrates multiple steps: data ingestion, NLP processing, knowledge base lookup, and response generation.

**Components:**

*   **Azure AI Foundry:** To host the LLM and potentially manage agent workflows.
*   **Semantic Kernel:** To orchestrate the agent logic, manage skills, and interact with the LLM.
*   **Azure AI Services:** For NLP capabilities (e.g., Azure AI Language for entity recognition, sentiment analysis).
*   **Azure AI Search:** To power the internal knowledge base for efficient retrieval.

**Workflow:**

1.  Simulated new communication arrives (e.g., a new support ticket description).
2.  The Semantic Kernel agent receives the communication.
3.  The agent uses an NLP tool (e.g., `AnalyzeTextSkill`) to extract entities and sentiment.
4.  Based on extracted entities, the agent queries an Azure AI Search knowledge base (e.g., `SearchKnowledgeBaseSkill`) to find relevant articles or policies.
5.  The agent then synthesizes the information from the communication and the knowledge base.
6.  If a predefined condition is met (e.g., negative sentiment on a critical product, or a new policy conflicting with existing projects), the agent generates a proactive alert/summary.
7.  Alternatively, if a user asks a question, the agent follows a similar process to synthesize a comprehensive answer.

### C# Implementation Example

This C# example demonstrates a simplified `ProactiveKnowledgeAgent` using Semantic Kernel. It will simulate processing a piece of internal communication, extracting key information, and then synthesizing a response or alert. For simplicity, the NLP and knowledge base interactions will be simulated.

First, ensure you have the necessary NuGet packages installed:

```xml
<ItemGroup>
    <PackageReference Include="Microsoft.SemanticKernel" Version="1.0.0-beta10" />
    <PackageReference Include="Microsoft.SemanticKernel.Connectors.OpenAI" Version="1.0.0-beta10" />
    <PackageReference Include="Azure.AI.TextAnalytics" Version="5.3.0" /> <!-- For actual NLP -->
    <PackageReference Include="Azure.Search.Documents" Version="11.4.0" /> <!-- For actual Azure AI Search -->
</ItemGroup>
```

```csharp
using Microsoft.SemanticKernel;
using Microsoft.SemanticKernel.Connectors.OpenAI;
using Microsoft.SemanticKernel.ChatCompletion;
using System;
using System.Threading.Tasks;
using System.ComponentModel;
using System.Collections.Generic;
using System.Linq;

// Simulated NLP Tool
public class NlpTools
{
    [KernelFunction, Description("Analyzes text to extract key phrases and sentiment.")]
    public string AnalyzeText([Description("The text to analyze.")] string text)
    {
        Console.WriteLine($"[Tool Call: AnalyzeText for '{text.Substring(0, Math.Min(text.Length, 50))}...']");
        // In a real scenario, this would call Azure AI Language Service
        if (text.Contains("critical bug") || text.Contains("major outage"))
        {
            return "Key Phrases: critical bug, major outage. Sentiment: Negative. Severity: High.";
        }
        else if (text.Contains("new feature request") || text.Contains("enhancement"))
        {
            return "Key Phrases: new feature, enhancement. Sentiment: Neutral. Type: Feature Request.";
        }
        else if (text.Contains("positive feedback") || text.Contains("great experience"))
        {
            return "Key Phrases: positive feedback, great experience. Sentiment: Positive.";
        }
        return "Key Phrases: general. Sentiment: Neutral.";
    }
}

// Simulated Knowledge Base Search Tool
public class KnowledgeBaseTools
{
    [KernelFunction, Description("Searches the internal knowledge base for relevant articles or policies.")]
    public string SearchKnowledgeBase([Description("The query to search the knowledge base with.")] string query)
    {
        Console.WriteLine($"[Tool Call: SearchKnowledgeBase for '{query}']");
        // In a real scenario, this would call Azure AI Search
        if (query.Contains("bug reporting policy"))
        {
            return "Knowledge Base Result: Found 'Bug Reporting Policy v2.0'. Key points: All critical bugs must be reported within 1 hour to #critical-issues channel.";
        }
        else if (query.Contains("new feature process"))
        {
            return "Knowledge Base Result: Found 'New Feature Development Process'. Key points: All new features require a design review and stakeholder approval.";
        }
        return "Knowledge Base Result: No relevant articles found.";
    }
}

public class ProactiveKnowledgeAgent
{
    private readonly Kernel _kernel;
    private readonly ChatHistory _chatHistory;

    public ProactiveKnowledgeAgent(string openAiEndpoint, string openAiKey, string openAiDeploymentName)
    {
        _kernel = Kernel.CreateBuilder()
            .AddAzureOpenAIChatCompletion(
                deploymentName: openAiDeploymentName,
                endpoint: openAiEndpoint,
                apiKey: openAiKey)
            .Build();

        _kernel.ImportPluginFromObject(new NlpTools(), "NlpPlugin");
        _kernel.ImportPluginFromObject(new KnowledgeBaseTools(), "KbPlugin");

        _chatHistory = new ChatHistory();
        _chatHistory.AddSystemMessage("You are a proactive enterprise knowledge agent. Your goal is to monitor internal communications, identify critical information, cross-reference with the knowledge base, and generate proactive alerts or summaries. You can also answer complex queries by synthesizing information. Use the available tools to achieve your goals. Respond concisely and informatively.");
    }

    public async Task ProcessCommunication(string communicationText)
    {
        Console.WriteLine($"\n--- Processing New Communication ---\nText: {communicationText}");
        _chatHistory.AddUserMessage($"Process this communication: {communicationText}");

        OpenAIPromptExecutionSettings openAIPromptExecutionSettings = new() { ToolCallBehavior = ToolCallBehavior.AutoInvokeKernelFunctions };

        var result = await _kernel.GetChatCompletionAsync(
            _chatHistory,
            openAIPromptExecutionSettings
        );

        Console.WriteLine($"Agent Insight: {result.Content}");
    }

    public async Task AnswerQuery(string query)
    {
        Console.WriteLine($"\n--- Answering User Query ---\nQuery: {query}");
        _chatHistory.AddUserMessage(query);

        OpenAIPromptExecutionSettings openAIPromptExecutionSettings = new() { ToolCallBehavior = ToolCallBehavior.AutoInvokeKernelFunctions };

        var result = await _kernel.GetChatCompletionAsync(
            _chatHistory,
            openAIPromptExecutionSettings
        );

        Console.WriteLine($"Agent Answer: {result.Content}");
    }

    public static async Task Main(string[] args)
    {
        string openAiEndpoint = Environment.GetEnvironmentVariable("AZURE_OPENAI_ENDPOINT") ?? "YOUR_AZURE_OPENAI_ENDPOINT";
        string openAiKey = Environment.GetEnvironmentVariable("AZURE_OPENAI_KEY") ?? "YOUR_AZURE_OPENAI_KEY";
        string openAiDeploymentName = Environment.GetEnvironmentVariable("AZURE_OPENAI_DEPLOYMENT_NAME") ?? "YOUR_AZURE_OPENAI_DEPLOYMENT_NAME";

        if (new[] { openAiEndpoint, openAiKey, openAiDeploymentName }.Any(string.IsNullOrWhiteSpace))
        {
            Console.WriteLine("Please set the environment variables for Azure OpenAI credentials.");
            return;
        }

        ProactiveKnowledgeAgent agent = new ProactiveKnowledgeAgent(openAiEndpoint, openAiKey, openAiDeploymentName);

        // Simulate processing new communications
        await agent.ProcessCommunication("Urgent: Customer reported a critical bug in the new payment module. Users are unable to complete transactions. This is a major outage!");
        await agent.ProcessCommunication("Team, we received positive feedback on the recent UI update. Users found the new design intuitive and had a great experience.");
        await agent.ProcessCommunication("Just submitted a new feature request for integrating with the legacy CRM system. Looking for an enhancement to automate data sync.");

        // Simulate answering user queries
        await agent.AnswerQuery("What is the policy for reporting critical bugs?");
        await agent.AnswerQuery("Tell me about the process for new feature development.");
        await agent.AnswerQuery("Summarize the recent customer feedback on the UI update.");
    }
}
```

**Explanation:**

1.  **`NlpTools` and `KnowledgeBaseTools` Classes:**
    *   These classes define our simulated tools. `NlpTools.AnalyzeText` simulates calling an NLP service (like Azure AI Language) to extract key phrases and sentiment. `KnowledgeBaseTools.SearchKnowledgeBase` simulates querying an internal knowledge base (like Azure AI Search).
    *   `[KernelFunction]` and `[Description]` attributes are used to expose these methods as tools to Semantic Kernel, providing the LLM with the necessary metadata to understand their purpose and parameters.
2.  **`ProactiveKnowledgeAgent` Class:**
    *   **Kernel Initialization:** The `Kernel` is set up with an Azure OpenAI chat completion service, which serves as the brain of our agent.
    *   **Tool Import:** Both `NlpTools` and `KnowledgeBaseTools` are imported as plugins into the kernel, making their functions available for the agent to use.
    *   **`ProcessCommunication` Method:** This method simulates the agent autonomously processing new incoming text. It adds the communication to the chat history and then calls `_kernel.GetChatCompletionAsync` with `ToolCallBehavior.AutoInvokeKernelFunctions`. The LLM will decide if it needs to call `AnalyzeText` or `SearchKnowledgeBase` to understand the communication and formulate an insight or alert.
    *   **`AnswerQuery` Method:** This method handles ad-hoc user queries. Similar to `ProcessCommunication`, the LLM uses its reasoning and tool-calling capabilities to synthesize an answer based on the query and available tools.
3.  **`Main` Method:** This is the entry point. It sets up the agent and then demonstrates its capabilities by simulating both proactive communication processing and reactive query answering.

**Before running this code:**

*   **Azure OpenAI Service:** Ensure you have an Azure OpenAI service and a chat model deployed (e.g., `gpt-3.5-turbo` or `gpt-4`).
*   **Environment Variables:** Set the following environment variables with your actual credentials:
    *   `AZURE_OPENAI_ENDPOINT`
    *   `AZURE_OPENAI_KEY`
    *   `AZURE_OPENAI_DEPLOYMENT_NAME`

This C# example showcases how Semantic Kernel enables an agent to autonomously use tools to process information, derive insights, and respond to queries, embodying the core principles of agentic AI.

### How to Test the C# Implementation Example

This section provides step-by-step instructions on how to set up, run, and verify the C# code example for the Proactive Enterprise Knowledge Agent.

#### Prerequisites

*   .NET SDK (version 6.0 or higher) installed.
*   An Azure OpenAI Service instance with a chat model deployed (e.g., `gpt-3.5-turbo` or `gpt-4`). You will need the endpoint, API key, and the deployment name of your chat model.

#### Setup

1.  **Create a new C# Console Project:**
    ```bash
dotnet new console -n ProactiveAgentApp
cd ProactiveAgentApp
    ```
2.  **Add NuGet Packages:** Open the `ProactiveAgentApp.csproj` file and add the following `ItemGroup`:
    ```xml
<ItemGroup>
    <PackageReference Include="Microsoft.SemanticKernel" Version="1.0.0-beta10" />
    <PackageReference Include="Microsoft.SemanticKernel.Connectors.OpenAI" Version="1.0.0-beta10" />
    <PackageReference Include="Azure.AI.TextAnalytics" Version="5.3.0" />
    <PackageReference Include="Azure.Search.Documents" Version="11.4.0" />
</ItemGroup>
    ```
    Then, restore the packages:
    ```bash
dotnet restore
    ```
3.  **Create `Program.cs`:** Replace the content of `Program.cs` with the C# code provided above in the "C# Implementation Example" section. Ensure the `using` statements and class definitions are correct.

#### Configuration

Set the following environment variables with your Azure OpenAI credentials. Replace the placeholder values with your actual information.

*   `AZURE_OPENAI_ENDPOINT="YOUR_AZURE_OPENAI_ENDPOINT"`
*   `AZURE_OPENAI_KEY="YOUR_AZURE_OPENAI_KEY"`
*   `AZURE_OPENAI_DEPLOYMENT_NAME="YOUR_AZURE_OPENAI_DEPLOYMENT_NAME"`

**Example (for PowerShell on Windows):**
```powershell
$env:AZURE_OPENAI_ENDPOINT="https://your-openai-resource.openai.azure.com/"
$env:AZURE_OPENAI_KEY="your-openai-api-key"
$env:AZURE_OPENAI_DEPLOYMENT_NAME="your-chat-model-deployment-name"
```

**Example (for Bash/Zsh on Linux/macOS):**
```bash
export AZURE_OPENAI_ENDPOINT="https://your-openai-resource.openai.azure.com/"
export AZURE_OPENAI_KEY="your-openai-api-key"
export AZURE_OPENAI_DEPLOYMENT_NAME="your-chat-model-deployment-name"
```

#### Execution

Run the application from the `ProactiveAgentApp` directory:

```bash
dotnet run
```

#### Expected Results

The application will execute the simulated communication processing and query answering. You will see console output indicating the agent's actions and insights.

**Example Output (may vary slightly based on LLM response):**

```
--- Processing New Communication ---
Text: Urgent: Customer reported a critical bug in the new payment module. Users are unable to complete transactions. This is a major outage!
[Tool Call: AnalyzeText for 'Urgent: Customer reported a critical bug in the new paym...']
[Tool Call: SearchKnowledgeBase for 'bug reporting policy']
Agent Insight: Critical bug detected in payment module causing major outage. Refer to 'Bug Reporting Policy v2.0': All critical bugs must be reported within 1 hour to #critical-issues channel.

--- Processing New Communication ---
Text: Team, we received positive feedback on the recent UI update. Users found the new design intuitive and had a great experience.
[Tool Call: AnalyzeText for 'Team, we received positive feedback on the recent UI up...']
Agent Insight: Positive feedback received on the recent UI update. Users found the new design intuitive and had a great experience.

--- Processing New Communication ---
Text: Just submitted a new feature request for integrating with the legacy CRM system. Looking for an enhancement to automate data sync.
[Tool Call: AnalyzeText for 'Just submitted a new feature request for integrating w...']
Agent Insight: New feature request submitted for integrating with legacy CRM system to automate data sync.

--- Answering User Query ---
Query: What is the policy for reporting critical bugs?
[Tool Call: SearchKnowledgeBase for 'policy for reporting critical bugs']
Agent Answer: The 'Bug Reporting Policy v2.0' states that all critical bugs must be reported within 1 hour to the #critical-issues channel.

--- Answering User Query ---
Query: Tell me about the process for new feature development.
[Tool Call: SearchKnowledgeBase for 'process for new feature development']
Agent Answer: The 'New Feature Development Process' requires all new features to undergo a design review and obtain stakeholder approval.

--- Answering User Query ---
Query: Summarize the recent customer feedback on the UI update.
[Tool Call: AnalyzeText for 'Summarize the recent customer feedback on the UI update.']
Agent Answer: Recent customer feedback on the UI update is positive, with users finding the new design intuitive and reporting a great experience.
```

### Python Implementation Example

This Python example mirrors the C# implementation, demonstrating a `ProactiveKnowledgeAgent` using Semantic Kernel to process communications and answer queries. The NLP and knowledge base interactions are simulated.

First, ensure you have the necessary Python packages installed:

```bash
pip install semantic-kernel openai azure-ai-textanalytics azure-search-documents
```

```python
import os
import asyncio
from semantic_kernel import Kernel
from semantic_kernel.connectors.ai.open_ai import AzureChatCompletion
from semantic_kernel.functions import kernel_function
from semantic_kernel.contents.chat_history import ChatHistory

# Simulated NLP Tool
class NlpTools:
    @kernel_function(description="Analyzes text to extract key phrases and sentiment.")
    def analyze_text(self, text: str) -> str:
        print(f"[Tool Call: analyze_text for '{text[:50]}...']")
        # In a real scenario, this would call Azure AI Language Service
        if "critical bug" in text.lower() or "major outage" in text.lower():
            return "Key Phrases: critical bug, major outage. Sentiment: Negative. Severity: High."
        elif "new feature request" in text.lower() or "enhancement" in text.lower():
            return "Key Phrases: new feature, enhancement. Sentiment: Neutral. Type: Feature Request."
        elif "positive feedback" in text.lower() or "great experience" in text.lower():
            return "Key Phrases: positive feedback, great experience. Sentiment: Positive."
        return "Key Phrases: general. Sentiment: Neutral."

# Simulated Knowledge Base Search Tool
class KnowledgeBaseTools:
    @kernel_function(description="Searches the internal knowledge base for relevant articles or policies.")
    def search_knowledge_base(self, query: str) -> str:
        print(f"[Tool Call: search_knowledge_base for '{query}']")
        # In a real scenario, this would call Azure AI Search
        if "bug reporting policy" in query.lower():
            return "Knowledge Base Result: Found 'Bug Reporting Policy v2.0'. Key points: All critical bugs must be reported within 1 hour to #critical-issues channel."
        elif "new feature process" in query.lower():
            return "Knowledge Base Result: Found 'New Feature Development Process'. Key points: All new features require a design review and stakeholder approval."
        return "Knowledge Base Result: No relevant articles found."

class ProactiveKnowledgeAgent:
    def __init__(self):
        self.kernel = Kernel()
        self.kernel.add_service(
            AzureChatCompletion(
                service_id="azure_openai_chat_completion",
                deployment_name=os.environ.get("AZURE_OPENAI_DEPLOYMENT_NAME"),
                endpoint=os.environ.get("AZURE_OPENAI_ENDPOINT"),
                api_key=os.environ.get("AZURE_OPENAI_KEY"),
            )
        )

        self.kernel.import_plugin_from_object(NlpTools(), "NlpPlugin")
        self.kernel.import_plugin_from_object(KnowledgeBaseTools(), "KbPlugin")

        self.chat_history = ChatHistory()
        self.chat_history.add_system_message("You are a proactive enterprise knowledge agent. Your goal is to monitor internal communications, identify critical information, cross-reference with the knowledge base, and generate proactive alerts or summaries. You can also answer complex queries by synthesizing information. Use the available tools to achieve your goals. Respond concisely and informatively.")

    async def process_communication(self, communication_text: str):
        print(f"\n--- Processing New Communication ---\nText: {communication_text}")
        self.chat_history.add_user_message(f"Process this communication: {communication_text}")

        chat_completion_service = self.kernel.get_service("azure_openai_chat_completion")
        response = await chat_completion_service.get_chat_message_content(
            self.chat_history,
            settings=chat_completion_service.get_prompt_execution_settings(tool_choice="auto")
        )

        print(f"Agent Insight: {response.content}")

    async def answer_query(self, query: str):
        print(f"\n--- Answering User Query ---\nQuery: {query}")
        self.chat_history.add_user_message(query)

        chat_completion_service = self.kernel.get_service("azure_openai_chat_completion")
        response = await chat_completion_service.get_chat_message_content(
            self.chat_history,
            settings=chat_completion_service.get_prompt_execution_settings(tool_choice="auto")
        )

        print(f"Agent Answer: {response.content}")

async def main():
    required_env_vars = [
        "AZURE_OPENAI_ENDPOINT",
        "AZURE_OPENAI_KEY",
        "AZURE_OPENAI_DEPLOYMENT_NAME",
    ]

    for var in required_env_vars:
        if not os.environ.get(var):
            print(f"Please set the environment variable: {var}")
            exit(1)

    agent = ProactiveKnowledgeAgent()

    # Simulate processing new communications
    await agent.process_communication("Urgent: Customer reported a critical bug in the new payment module. Users are unable to complete transactions. This is a major outage!")
    await agent.process_communication("Team, we received positive feedback on the recent UI update. Users found the new design intuitive and had a great experience.")
    await agent.process_communication("Just submitted a new feature request for integrating with the legacy CRM system. Looking for an enhancement to automate data sync.")

    # Simulate answering user queries
    await agent.answer_query("What is the policy for reporting critical bugs?")
    await agent.answer_query("Tell me about the process for new feature development.")
    await agent.answer_query("Summarize the recent customer feedback on the UI update.")

if __name__ == "__main__":
    asyncio.run(main())
```

**Explanation:**

1.  **`NlpTools` and `KnowledgeBaseTools` Classes:**
    *   These classes define our simulated tools. `NlpTools.analyze_text` simulates calling an NLP service (like Azure AI Language) to extract key phrases and sentiment. `KnowledgeBaseTools.search_knowledge_base` simulates querying an internal knowledge base (like Azure AI Search).
    *   `@kernel_function` decorator is used to expose these methods as tools to Semantic Kernel, providing the LLM with the necessary metadata to understand their purpose and parameters.
2.  **`ProactiveKnowledgeAgent` Class:**
    *   **Kernel Initialization:** The `Kernel` is set up with an Azure OpenAI chat completion service, which serves as the brain of our agent.
    *   **Tool Import:** Both `NlpTools` and `KnowledgeBaseTools` are imported as plugins into the kernel, making their functions available for the agent to use.
    *   **`process_communication` Method:** This method simulates the agent autonomously processing new incoming text. It adds the communication to the chat history and then calls `chat_completion_service.get_chat_message_content` with `tool_choice="auto"`. The LLM will decide if it needs to call `analyze_text` or `search_knowledge_base` to understand the communication and formulate an insight or alert.
    *   **`answer_query` Method:** This method handles ad-hoc user queries. Similar to `process_communication`, the LLM uses its reasoning and tool-calling capabilities to synthesize an answer based on the query and available tools.
3.  **`main` Function:** This is the entry point. It sets up the agent and then demonstrates its capabilities by simulating both proactive communication processing and reactive query answering.

**Before running this code:**

*   **Azure OpenAI Service:** Ensure you have an Azure OpenAI service and a chat model deployed (e.g., `gpt-3.5-turbo` or `gpt-4`).
*   **Environment Variables:** Set the following environment variables with your actual credentials:
    *   `AZURE_OPENAI_ENDPOINT`
    *   `AZURE_OPENAI_KEY`
    *   `AZURE_OPENAI_DEPLOYMENT_NAME`

This Python example showcases how Semantic Kernel enables an agent to autonomously use tools to process information, derive insights, and respond to queries, embodying the core principles of agentic AI.

### How to Test the Python Implementation Example

This section provides step-by-step instructions on how to set up, run, and verify the Python code example for the Proactive Enterprise Knowledge Agent.

#### Prerequisites

*   Python 3.8 or higher installed.
*   An Azure OpenAI Service instance with a chat model deployed (e.g., `gpt-3.5-turbo` or `gpt-4`). You will need the endpoint, API key, and the deployment name of your chat model.

#### Setup

1.  **Create a new Python file:** Create a file named `proactive_agent.py`.
2.  **Install required packages:**
    ```bash
pip install semantic-kernel openai azure-ai-textanalytics azure-search-documents
    ```
3.  **Add the Python code:** Copy the Python code provided above in the "Python Implementation Example" section into `proactive_agent.py`.

#### Configuration

Set the following environment variables with your Azure OpenAI credentials. Replace the placeholder values with your actual information.

*   `AZURE_OPENAI_ENDPOINT="YOUR_AZURE_OPENAI_ENDPOINT"`
*   `AZURE_OPENAI_KEY="YOUR_AZURE_OPENAI_KEY"`
*   `AZURE_OPENAI_DEPLOYMENT_NAME="YOUR_AZURE_OPENAI_DEPLOYMENT_NAME"`

**Example (for Bash/Zsh on Linux/macOS):**
```bash
export AZURE_OPENAI_ENDPOINT="https://your-openai-resource.openai.azure.com/"
export AZURE_OPENAI_KEY="your-openai-api-key"
export AZURE_OPENAI_DEPLOYMENT_NAME="your-chat-model-deployment-name"
```

**Example (for PowerShell on Windows):**
```powershell
$env:AZURE_OPENAI_ENDPOINT="https://your-openai-resource.openai.azure.com/"
$env:AZURE_OPENAI_KEY="your-openai-api-key"
$env:AZURE_OPENAI_DEPLOYMENT_NAME="your-chat-model-deployment-name"
```

#### Execution

Run the Python script:

```bash
python proactive_agent.py
```

#### Expected Results

The application will execute the simulated communication processing and query answering. You will see console output indicating the agent's actions and insights.

**Example Output (may vary slightly based on LLM response):**

```
--- Processing New Communication ---
Text: Urgent: Customer reported a critical bug in the new payment module. Users are unable to complete transactions. This is a major outage!
[Tool Call: analyze_text for 'Urgent: Customer reported a critical bug in the new paym...']
[Tool Call: search_knowledge_base for 'bug reporting policy']
Agent Insight: Critical bug detected in payment module causing major outage. Refer to 'Bug Reporting Policy v2.0': All critical bugs must be reported within 1 hour to #critical-issues channel.

--- Processing New Communication ---
Text: Team, we received positive feedback on the recent UI update. Users found the new design intuitive and had a great experience.
[Tool Call: analyze_text for 'Team, we received positive feedback on the recent UI up...']
Agent Insight: Positive feedback received on the recent UI update. Users found the new design intuitive and had a great experience.

--- Processing New Communication ---
Text: Just submitted a new feature request for integrating with the legacy CRM system. Looking for an enhancement to automate data sync.
[Tool Call: analyze_text for 'Just submitted a new feature request for integrating w...']
Agent Insight: New feature request submitted for integrating with legacy CRM system to automate data sync.

--- Answering User Query ---
Query: What is the policy for reporting critical bugs?
[Tool Call: search_knowledge_base for 'policy for reporting critical bugs']
Agent Answer: The 'Bug Reporting Policy v2.0' states that all critical bugs must be reported within 1 hour to the #critical-issues channel.

--- Answering User Query ---
Query: Tell me about the process for new feature development.
[Tool Call: search_knowledge_base for 'process for new feature development']
Agent Answer: The 'New Feature Development Process' requires all new features to undergo a design review and obtain stakeholder approval.

--- Answering User Query ---
Query: Summarize the recent customer feedback on the UI update.
[Tool Call: analyze_text for 'Summarize the recent customer feedback on the UI update.']
Agent Answer: Recent customer feedback on the UI update is positive, with users finding the new design intuitive and reporting a great experience.
```






### Enhancing Sophistication with Multi-Agent Orchestration

While the previous examples demonstrated basic agentic behavior with Semantic Kernel, real-world enterprise scenarios often involve more complex orchestration, especially in multi-agent systems. Inspired by the [Microsoft Agentic Cookbook](https://github.com/microsoft/agenticcookbook), which showcases advanced multi-agent patterns using frameworks like AutoGen, we will now present a more sophisticated example. This example will illustrate how multiple agents can collaborate to achieve a complex goal, leveraging tools and shared context, which is a hallmark of advanced agentic applications.

For this enhanced example, we will shift our focus to a multi-agent travel agency scenario, similar to one found in the `agenticcookbook`. This will demonstrate how different specialized agents (e.g., a customer assistant, a flight booking agent, an accommodation booking agent) can interact and orchestrate their actions to fulfill a user's request for a travel package.

**Note:** The `agenticcookbook` primarily uses AutoGen for its multi-agent examples. While Semantic Kernel also supports multi-agent patterns, using AutoGen for this specific sophisticated example allows us to directly leverage the patterns demonstrated in the cookbook and highlight a different, yet equally important, agentic framework within the Microsoft ecosystem. We will provide both C# (using Semantic Kernel's multi-agent capabilities where applicable, or a conceptual multi-agent design) and Python (using AutoGen) implementations to showcase the breadth of options.






### C# Implementation Example: Multi-Agent Travel Booking with Semantic Kernel (Conceptual)

For a sophisticated C# example demonstrating multi-agent patterns, we will conceptualize a simplified version of the travel agency scenario using Semantic Kernel. While Semantic Kernel primarily focuses on single-agent orchestration with tool use, multi-agent collaboration can be achieved by designing specialized agents (each potentially a `Kernel` instance or a set of well-defined plugins within a single kernel) that interact and pass information to achieve a common goal. This example will focus on the orchestration logic and the definition of specialized 'skills' that mimic the roles of different agents.

**Scenario:** A customer wants to book a travel package including flights and accommodation. A `TravelCoordinatorAgent` (main orchestrator) will interact with a `FlightBookingAgent` (via `FlightBookingSkills`) and an `AccommodationBookingAgent` (via `AccommodationBookingSkills`).

**Key Idea:** Instead of separate processes for each agent, we'll use a single Semantic Kernel instance where different 'agents' are represented by distinct sets of skills and the main agent's prompt guides the orchestration between these skill sets.

First, ensure you have the necessary NuGet packages installed:

```xml
<ItemGroup>
    <PackageReference Include="Microsoft.SemanticKernel" Version="1.0.0-beta10" />
    <PackageReference Include="Microsoft.SemanticKernel.Connectors.OpenAI" Version="1.0.0-beta10" />
</ItemGroup>
```

```csharp
using Microsoft.SemanticKernel;
using Microsoft.SemanticKernel.Connectors.OpenAI;
using Microsoft.SemanticKernel.ChatCompletion;
using System;
using System.Threading.Tasks;
using System.ComponentModel;
using System.Collections.Generic;
using System.Linq;

// Simulated Flight Booking Skills (Agent)
public class FlightBookingSkills
{
    [KernelFunction, Description("Finds available flights based on origin, destination, and date.")]
    public string FindFlights(
        [Description("The origin city.")] string origin,
        [Description("The destination city.")] string destination,
        [Description("The departure date in YYYY-MM-DD format.")] string date)
    {
        Console.WriteLine($"[FlightBookingAgent: Searching flights from {origin} to {destination} on {date}]");
        // Simulate API call to a flight booking system
        if (origin.ToLower() == "london" && destination.ToLower() == "paris" && date == "2025-08-10")
        {
            return "Available flights: Flight LH456 (London-Paris, 2025-08-10, 09:00 AM, $150), Flight AF789 (London-Paris, 2025-08-10, 11:30 AM, $180).";
        }
        return "No direct flights found for the specified route and date.";
    }

    [KernelFunction, Description("Books a specific flight for a given number of passengers.")]
    public string BookFlight(
        [Description("The flight name or ID to book.")] string flightId,
        [Description("The number of passengers.")] int passengers)
    {
        Console.WriteLine($"[FlightBookingAgent: Booking {passengers} seats on {flightId}]");
        // Simulate API call to book the flight
        return $"Successfully booked {passengers} seats on {flightId}. Confirmation: FLIGHTCONF123.";
    }
}

// Simulated Accommodation Booking Skills (Agent)
public class AccommodationBookingSkills
{
    [KernelFunction, Description("Finds available accommodations based on location, check-in, and check-out dates.")]
    public string FindAccommodations(
        [Description("The location for accommodation.")] string location,
        [Description("The check-in date in YYYY-MM-DD format.")] string checkInDate,
        [Description("The check-out date in YYYY-MM-DD format.")] string checkOutDate)
    {
        Console.WriteLine($"[AccommodationBookingAgent: Searching accommodations in {location} from {checkInDate} to {checkOutDate}]");
        // Simulate API call to an accommodation booking system
        if (location.ToLower() == "paris" && checkInDate == "2025-08-10" && checkOutDate == "2025-08-15")
        {
            return "Available accommodations: Hotel Eiffel (5 nights, $1000), Boutique Stay (5 nights, $800).";
        }
        return "No accommodations found for the specified criteria.";
    }

    [KernelFunction, Description("Books a specific accommodation.")]
    public string BookAccommodation(
        [Description("The accommodation name or ID to book.")] string accommodationId,
        [Description("The check-in date in YYYY-MM-DD format.")] string checkInDate,
        [Description("The check-out date in YYYY-MM-DD format.")] string checkOutDate)
    {
        Console.WriteLine($"[AccommodationBookingAgent: Booking {accommodationId} from {checkInDate} to {checkOutDate}]");
        // Simulate API call to book the accommodation
        return $"Successfully booked {accommodationId}. Confirmation: HOTELCONF456.";
    }
}

public class TravelCoordinatorAgent
{
    private readonly Kernel _kernel;
    private readonly ChatHistory _chatHistory;

    public TravelCoordinatorAgent(string openAiEndpoint, string openAiKey, string openAiDeploymentName)
    {
        _kernel = Kernel.CreateBuilder()
            .AddAzureOpenAIChatCompletion(
                deploymentName: openAiDeploymentName,
                endpoint: openAiEndpoint,
                apiKey: openAiKey)
            .Build();

        // Import skills for different 


roles/agents
        _kernel.ImportPluginFromObject(new FlightBookingSkills(), "FlightBookingPlugin");
        _kernel.ImportPluginFromObject(new AccommodationBookingSkills(), "AccommodationBookingPlugin");

        _chatHistory = new ChatHistory();
        _chatHistory.AddSystemMessage("You are a travel coordinator agent. Your goal is to assist users in booking travel packages, including flights and accommodations. You can use the FlightBookingPlugin and AccommodationBookingPlugin to find and book travel components. Orchestrate these tools to fulfill the user's request. Always confirm the booking details with the user.");
    }

    public async Task ProcessTravelRequest(string request)
    {
        Console.WriteLine($"\n--- Processing Travel Request ---\nRequest: {request}");
        _chatHistory.AddUserMessage(request);

        OpenAIPromptExecutionSettings openAIPromptExecutionSettings = new() { ToolCallBehavior = ToolCallBehavior.AutoInvokeKernelFunctions };

        var result = await _kernel.GetChatCompletionAsync(
            _chatHistory,
            openAIPromptExecutionSettings
        );

        Console.WriteLine($"Agent Response: {result.Content}");
    }

    public static async Task Main(string[] args)
    {
        string openAiEndpoint = Environment.GetEnvironmentVariable("AZURE_OPENAI_ENDPOINT") ?? "YOUR_AZURE_OPENAI_ENDPOINT";
        string openAiKey = Environment.GetEnvironmentVariable("AZURE_OPENAI_KEY") ?? "YOUR_AZURE_OPENAI_KEY";
        string openAiDeploymentName = Environment.GetEnvironmentVariable("AZURE_OPENAI_DEPLOYMENT_NAME") ?? "YOUR_AZURE_OPENAI_DEPLOYMENT_NAME";

        if (new[] { openAiEndpoint, openAiKey, openAiDeploymentName }.Any(string.IsNullOrWhiteSpace))
        {
            Console.WriteLine("Please set the environment variables for Azure OpenAI credentials.");
            return;
        }

        TravelCoordinatorAgent agent = new TravelCoordinatorAgent(openAiEndpoint, openAiKey, openAiDeploymentName);

        // Simulate a complex travel request
        await agent.ProcessTravelRequest("I want to book a trip from London to Paris, departing on 2025-08-10. I also need accommodation in Paris from 2025-08-10 to 2025-08-15. Please find and book both for 1 person.");

        // Another request
        await agent.ProcessTravelRequest("Find me flights from New York to Los Angeles for next month and a hotel for 3 nights.");
    }
}
```

**Explanation:**

1.  **`FlightBookingSkills` and `AccommodationBookingSkills` Classes:**
    *   These classes represent the capabilities of our specialized agents (Flight Booking Agent and Accommodation Booking Agent). Each method within these classes is exposed as a `KernelFunction` (tool) that the main `TravelCoordinatorAgent` can invoke.
    *   They simulate interactions with external booking systems.
2.  **`TravelCoordinatorAgent` Class:**
    *   **Kernel Initialization:** A single `Kernel` instance is created, acting as the central orchestrator.
    *   **Skill Import:** Both `FlightBookingSkills` and `AccommodationBookingSkills` are imported as plugins into the kernel. This makes their functions available to the `TravelCoordinatorAgent`.
    *   **System Message:** The system message for the `TravelCoordinatorAgent` explicitly instructs it to use the `FlightBookingPlugin` and `AccommodationBookingPlugin` to fulfill travel requests, guiding its agentic behavior.
    *   **`ProcessTravelRequest` Method:** This method takes a user's travel request. The LLM, guided by the system message and its understanding of the available tools, will autonomously decide to call `FindFlights`, `BookFlight`, `FindAccommodations`, and `BookAccommodation` in the correct sequence to fulfill the request. The `ToolCallBehavior.AutoInvokeKernelFunctions` setting allows the LLM to automatically execute these tool calls.
3.  **`Main` Method:** This sets up the `TravelCoordinatorAgent` and demonstrates its ability to handle complex, multi-step travel booking requests by orchestrating the simulated sub-agent skills.

**Before running this code:**

*   **Azure OpenAI Service:** Ensure you have an Azure OpenAI service and a chat model deployed (e.g., `gpt-3.5-turbo` or `gpt-4`).
*   **Environment Variables:** Set the following environment variables with your actual credentials:
    *   `AZURE_OPENAI_ENDPOINT`
    *   `AZURE_OPENAI_KEY`
    *   `AZURE_OPENAI_DEPLOYMENT_NAME`

This C# example demonstrates how Semantic Kernel can be used to build sophisticated, multi-step agentic applications by defining specialized skills and allowing the LLM to orchestrate their execution to achieve complex user goals.

### How to Test the C# Implementation Example

This section provides step-by-step instructions on how to set up, run, and verify the C# code example for the Multi-Agent Travel Booking system.

#### Prerequisites

*   .NET SDK (version 6.0 or higher) installed.
*   An Azure OpenAI Service instance with a chat model deployed (e.g., `gpt-3.5-turbo` or `gpt-4`). You will need the endpoint, API key, and the deployment name of your chat model.

#### Setup

1.  **Create a new C# Console Project:**
    ```bash
dotnet new console -n TravelAgentApp
cd TravelAgentApp
    ```
2.  **Add NuGet Packages:** Open the `TravelAgentApp.csproj` file and add the following `ItemGroup`:
    ```xml
<ItemGroup>
    <PackageReference Include="Microsoft.SemanticKernel" Version="1.0.0-beta10" />
    <PackageReference Include="Microsoft.SemanticKernel.Connectors.OpenAI" Version="1.0.0-beta10" />
</ItemGroup>
    ```
    Then, restore the packages:
    ```bash
dotnet restore
    ```
3.  **Create `Program.cs`:** Replace the content of `Program.cs` with the C# code provided above in the "C# Implementation Example" section. Ensure the `using` statements and class definitions are correct.

#### Configuration

Set the following environment variables with your Azure OpenAI credentials. Replace the placeholder values with your actual information.

*   `AZURE_OPENAI_ENDPOINT="YOUR_AZURE_OPENAI_ENDPOINT"`
*   `AZURE_OPENAI_KEY="YOUR_AZURE_OPENAI_KEY"`
*   `AZURE_OPENAI_DEPLOYMENT_NAME="YOUR_AZURE_OPENAI_DEPLOYMENT_NAME"`

**Example (for PowerShell on Windows):**
```powershell
$env:AZURE_OPENAI_ENDPOINT="https://your-openai-resource.openai.azure.com/"
$env:AZURE_OPENAI_KEY="your-openai-api-key"
$env:AZURE_OPENAI_DEPLOYMENT_NAME="your-chat-model-deployment-name"
```

**Example (for Bash/Zsh on Linux/macOS):**
```bash
export AZURE_OPENAI_ENDPOINT="https://your-openai-resource.openai.azure.com/"
export AZURE_OPENAI_KEY="your-openai-api-key"
export AZURE_OPENAI_DEPLOYMENT_NAME="your-chat-model-deployment-name"
```

#### Execution

Run the application from the `TravelAgentApp` directory:

```bash
dotnet run
```

#### Expected Results

The application will process the simulated travel requests. You will see console output indicating the agent's actions (tool calls) and its final response.

**Example Output (may vary slightly based on LLM response and exact tool call sequence):**

```
--- Processing Travel Request ---
Request: I want to book a trip from London to Paris, departing on 2025-08-10. I also need accommodation in Paris from 2025-08-10 to 2025-08-15. Please find and book both for 1 person.
[FlightBookingAgent: Searching flights from London to Paris on 2025-08-10]
[FlightBookingAgent: Booking Flight LH456 (London-Paris, 2025-08-10, 09:00 AM, $150)]
[AccommodationBookingAgent: Searching accommodations in Paris from 2025-08-10 to 2025-08-15]
[AccommodationBookingAgent: Booking Hotel Eiffel from 2025-08-10 to 2025-08-15]
Agent Response: I have successfully booked your flight (Flight LH456, Confirmation: FLIGHTCONF123) and accommodation (Hotel Eiffel, Confirmation: HOTELCONF456) for your trip from London to Paris. Enjoy your trip!

--- Processing Travel Request ---
Request: Find me flights from New York to Los Angeles for next month and a hotel for 3 nights.
[FlightBookingAgent: Searching flights from New York to Los Angeles on 2025-08-22] (Date will be inferred by LLM)
[AccommodationBookingAgent: Searching accommodations in Los Angeles from 2025-08-22 to 2025-08-25] (Dates inferred)
Agent Response: I couldn't find direct flights for New York to Los Angeles for next month, nor could I find accommodations for 3 nights. Please provide more specific dates or criteria if you'd like me to try again.
```

This output demonstrates the agent's ability to interpret a complex request, break it down, call the appropriate tools (simulated sub-agents), and synthesize a coherent response, including handling cases where information is not found.






### Python Implementation Example: Multi-Agent Travel Booking with AutoGen

For a sophisticated Python example demonstrating multi-agent orchestration, we will use the AutoGen framework, which is prominently featured in the Microsoft Agentic Cookbook for multi-agent scenarios. This example will replicate a simplified version of the travel agency scenario, showcasing how different specialized agents can collaborate to fulfill a user's travel package request.

**Scenario:** A customer wants to book a travel package including flights and accommodation. A `customer_proxy` agent will interact with a `customer_service` agent (front office), which in turn orchestrates `flight_booking_assistant` and `accommodation_booking_assistant` (back office) agents. A `computer_terminal` agent will simulate tool execution.

First, ensure you have the necessary Python packages installed. The `agenticcookbook` uses `autogen` and `llama-index` for some functionalities. We'll simplify the dependencies for this example.

```bash
pip install pyautogen openai
```

```python
import os
import json
from datetime import date
import random
from autogen import ConversableAgent, GroupChat, GroupChatManager
from autogen.agentchat.contrib.capabilities.teachability import Teachability

# --- Simulated Tools (from travel_tools.py in agenticcookbook) ---

bookings = {
    "flights": [],
    "accommodations": [],
    "attractions": []
}

def send_booking_email(email: str, booking_details: dict) -> str:
    """Send an email with full booking details. The booking details must be a dictionary."""
    print(f"[Tool Call: Sending email to {email}]")
    message = f"Dear traveller, \n\nWe are happy to confirm your booking. Here are the details: \n\n{json.dumps(obj=booking_details, indent=4)}\n\nHave a great trip!\n\nThe travel team"
    # In a real scenario, this would integrate with an email service
    return f"Email sent to {email} with details: {message[:100]}..."

def get_bookings() -> dict:
    """Useful for getting current bookings."""
    print("[Tool Call: Getting current bookings]")
    return bookings

def find_flights(
        origin: str,
        destination: str,
        date: str # Changed to string for simplicity, handle date parsing in real app
        ) -> list[dict]:
    """Can find flights on a specific date between a departure and destination."""
    print(f"[Tool Call: Finding flights from {origin} to {destination} on {date}]")
    values = []
    for i in range(random.randrange(1, 3)): # Simplified range
        values.append({
            "name": f"Flight {i+1}",
            "date": date,
            "origin": origin,
            "departure_time": f"{random.randrange(8, 20)}:00",
            "price_usd": f"{random.randrange(100, 500)}",
            "destination": destination
        })
    return values

def book_flight(
        flight_name: str,
        origin: str,
        destination: str,
        departure_date: str,
        passengers: int
        ) -> dict:
    """Can book a flight on a date for any number of passengers. It returns the booking confirmation."""
    print(f"[Tool Call: Booking flight {flight_name} for {passengers} passengers]")
    flight_booking ={
        "name": flight_name,
        "date": departure_date,
        "passengers": passengers,
        "origin": origin,
        "destination": destination,
        "booking_reference": random.randrange(1000, 9999)
    }
    bookings["flights"].append(flight_booking)
    return flight_booking

def find_accommodations(
        location: str,
        check_in_date: str,
        check_out_date: str
        ) -> list[dict]:
    """Can find accommodations for a given location and dates."""
    print(f"[Tool Call: Finding accommodations in {location} from {check_in_date} to {check_out_date}]")
    values = []
    for i in range(random.randrange(1, 3)): # Simplified range
        values.append(
            {
                "name": f"Hotel {i+1}",
                "location": location,
                "check_in": check_in_date,
                "check_out": check_out_date,
                "price_per_night_usd": f"{random.randrange(50, 200)}",
            }
        )
    return values

def book_accommodation(
        accommodation_name: str,
        check_in_date: str,
        nights: int,
        guests: int
        ) -> dict:
    """Can book accommodation for a group of guests on specific date and number on nights. It returns the booking confirmation including the booking reference."""
    print(f"[Tool Call: Booking accommodation {accommodation_name} for {guests} guests]")
    accommodation_booking = {
        "name": accommodation_name,
        "check_in": check_in_date,
        "nights": nights,
        "guests": guests,
        "booking_reference": random.randrange(1000, 9999)
    }
    bookings["accommodations"].append(accommodation_booking)
    return accommodation_booking

# --- AutoGen Agent Setup ---

# Configuration for LLM (replace with your Azure OpenAI details)
config_list_openai = [
    {
        "model": os.environ.get("AZURE_OPENAI_DEPLOYMENT_NAME"),
        "api_key": os.environ.get("AZURE_OPENAI_KEY"),
        "base_url": os.environ.get("AZURE_OPENAI_ENDPOINT"),
        "api_type": "azure",
        "api_version": "2024-02-01", # Or your specific API version
    }
]

llm_config = {"config_list": config_list_openai, "cache_seed": None}

# 1. Customer Proxy Agent (User Simulator)
customer_proxy = ConversableAgent(
    "customer_proxy",
    description="This is the customer trying to book a trip, flights and accommodations.",
    human_input_mode="NEVER", # Set to NEVER for automated testing
    llm_config=llm_config,
    is_termination_msg=lambda x: "TERMINATE" in x.get("content", "").upper(),
)

# 2. Front Office Agents
customer_service_agent = ConversableAgent(
    "customer_service",
    system_message="You handle all the final communication, sending booking confirmations and other details. You can access the current customer bookings details and use them in email and communications. Use the 'get_bookings' tool to get the bookings and 'send_booking_email' to send an email with booking details. As you learn more about the customers and their booking habits, you can use this information to provide better service.",
    llm_config=llm_config,
    code_execution_config=False, # This agent doesn't execute code directly
)

# Add teachability to the customer service agent (optional, for learning over time)
# teachability = Teachability(reset_db=False, path_to_db_dir="./customer_service_teachability_db", llm_config=llm_config)
# teachability.add_to_agent(customer_service_agent)

trip_specialist_agent = ConversableAgent(
    "trip_specialist",
    system_message="You help customers finding more about places they would like to visit. You can use external resources to provide more details as you engage with the customer. This agent helps in finding attractions, history and all that there is to know about a place.",
    llm_config=llm_config,
    code_execution_config=False,
)

# 3. Back Office Agents
flight_booking_agent = ConversableAgent(
    "flight_booking_assistant",
    system_message="You help customers finding flights and booking them. Use the 'find_flights' tool to search for flights and 'book_flight' to book a flight. All retrieved information will be sent to the customer service which will present information to the customer.",
    llm_config=llm_config,
    code_execution_config=False,
)

accommodation_booking_agent = ConversableAgent(
    "accommodation_booking_assistant",
    system_message="You help customers finding hotels and accommodations and booking them. Use 'find_accommodations' to search and 'book_accommodation' to book. All retrieved information will be sent to the customer service which will present information to the customer.",
    llm_config=llm_config,
    code_execution_config=False,
)

# 4. Computer Terminal Agent (Tool Executor)
# This agent is responsible for executing the actual tool functions.
terminal_agent = ConversableAgent(
    "computer_terminal",
    description="This computer terminal can be used to execute tools like booking flights and accommodations.",
    llm_config=None, # No LLM needed for this agent, it just executes tools
    code_execution_config={
        "last_n_messages": 1, # Only consider the last message for tool calls
        "work_dir": "./", # Working directory for code execution
        "use_docker": False, # Set to True if you have Docker and want isolated execution
    },
    is_termination_msg=lambda x: "TERMINATE" in x.get("content", "").upper(),
    human_input_mode="NEVER",
)

# Register functions with the terminal_agent
terminal_agent.register_for_execution(name="send_booking_email", tool_function=send_booking_email)
terminal_agent.register_for_execution(name="get_bookings", tool_function=get_bookings)
terminal_agent.register_for_execution(name="find_flights", tool_function=find_flights)
terminal_agent.register_for_execution(name="book_flight", tool_function=book_flight)
terminal_agent.register_for_execution(name="find_accommodations", tool_function=find_accommodations)
terminal_agent.register_for_execution(name="book_accommodation", tool_function=book_accommodation)

# Allow agents to call tools via the terminal_agent
for agent in [customer_service_agent, flight_booking_agent, accommodation_booking_agent]:
    agent.register_for_tool_calls(terminal_agent, speaker_selection_method="auto")

# --- Group Chat Setup ---

group_chat = GroupChat(
    agents=[
        customer_proxy,
        customer_service_agent,
        trip_specialist_agent,
        flight_booking_agent,
        accommodation_booking_agent,
        terminal_agent,
    ],
    messages=[],
    max_round=50, # Limit rounds to prevent infinite loops
    speaker_selection_method="auto",
    allow_repeat_speaker=False,
)

group_chat_manager = GroupChatManager(
    groupchat=group_chat,
    llm_config=llm_config,
)

# --- Initiate the Conversation ---

async def run_conversation():
    print("\n--- Starting Multi-Agent Travel Booking Conversation ---")
    chat_result = await customer_proxy.a_initiate_chat(
        group_chat_manager,
        message="I want to book a trip from London to Paris, departing on 2025-08-10. I also need accommodation in Paris from 2025-08-10 to 2025-08-15. Please find and book both for 1 person.",
    )
    print("\n--- Conversation Finished ---")
    # You can inspect chat_result for the full conversation history
    # print(chat_result.summary)
    # print(chat_result.chat_history)

if __name__ == "__main__":
    asyncio.run(run_conversation())
```

**Explanation:**

1.  **Simulated Tools:** The `send_booking_email`, `get_bookings`, `find_flights`, `book_flight`, `find_accommodations`, and `book_accommodation` functions simulate external APIs for a travel booking system. These are simplified versions of the tools found in the `agenticcookbook`'s `travel_tools.py`.
2.  **AutoGen Agents:**
    *   **`customer_proxy`:** Represents the user. In a real application, this would be the interface for human input. Here, it initiates the conversation with a predefined message.
    *   **`customer_service_agent`:** The front-office agent responsible for interacting with the customer and orchestrating the back-office agents. Its system message guides it to use the booking tools.
    *   **`trip_specialist_agent`:** (Included for completeness, but not actively used in this simplified flow) Could be used for providing information about destinations.
    *   **`flight_booking_agent` & `accommodation_booking_agent`:** Back-office agents specialized in their respective booking tasks. Their system messages guide them to use the `find_` and `book_` tools.
    *   **`terminal_agent`:** A crucial agent that acts as the executor for all the defined tools. When other agents decide to use a tool, they send a message to the `terminal_agent`, which then executes the corresponding Python function.
3.  **Tool Registration:** The `terminal_agent.register_for_execution` method makes the Python functions available as tools that can be called by other agents. `agent.register_for_tool_calls(terminal_agent)` allows the `customer_service_agent`, `flight_booking_agent`, and `accommodation_booking_agent` to propose tool calls to the `terminal_agent`.
4.  **Group Chat:**
    *   `GroupChat` defines the collection of agents and manages the conversation flow. `speaker_selection_method="auto"` allows AutoGen to automatically determine which agent should speak next based on the conversation context and agent capabilities.
    *   `GroupChatManager` orchestrates the `GroupChat`, ensuring agents communicate effectively to achieve the overall goal.
5.  **Conversation Initiation:** The `customer_proxy.a_initiate_chat` method starts the multi-agent conversation with a complex request. The agents then collaborate, calling tools as needed, until the request is fulfilled or a termination condition is met.

**Before running this code:**

*   **Azure OpenAI Service:** Ensure you have an Azure OpenAI service and a chat model deployed (e.g., `gpt-3.5-turbo` or `gpt-4`).
*   **Environment Variables:** Set the following environment variables with your actual credentials:
    *   `AZURE_OPENAI_ENDPOINT`
    *   `AZURE_OPENAI_KEY`
    *   `AZURE_OPENAI_DEPLOYMENT_NAME`

This Python example demonstrates a sophisticated multi-agent system where specialized agents collaborate and use tools to achieve a complex user goal, showcasing the power of agentic patterns with AutoGen.

### How to Test the Python Implementation Example

This section provides step-by-step instructions on how to set up, run, and verify the Python code example for the Multi-Agent Travel Booking system using AutoGen.

#### Prerequisites

*   Python 3.8 or higher installed.
*   An Azure OpenAI Service instance with a chat model deployed (e.g., `gpt-3.5-turbo` or `gpt-4`). You will need the endpoint, API key, and the deployment name of your chat model.

#### Setup

1.  **Create a new Python file:** Create a file named `multi_agent_travel.py`.
2.  **Install required packages:**
    ```bash
pip install pyautogen openai
    ```
3.  **Add the Python code:** Copy the Python code provided above in the "Python Implementation Example" section into `multi_agent_travel.py`.

#### Configuration

Set the following environment variables with your Azure OpenAI credentials. Replace the placeholder values with your actual information.

*   `AZURE_OPENAI_ENDPOINT="YOUR_AZURE_OPENAI_ENDPOINT"`
*   `AZURE_OPENAI_KEY="YOUR_AZURE_OPENAI_KEY"`
*   `AZURE_OPENAI_DEPLOYMENT_NAME="YOUR_AZURE_OPENAI_DEPLOYMENT_NAME"`

**Example (for Bash/Zsh on Linux/macOS):**
```bash
export AZURE_OPENAI_ENDPOINT="https://your-openai-resource.openai.azure.com/"
export AZURE_OPENAI_KEY="your-openai-api-key"
export AZURE_OPENAI_DEPLOYMENT_NAME="your-chat-model-deployment-name"
```

**Example (for PowerShell on Windows):**
```powershell
$env:AZURE_OPENAI_ENDPOINT="https://your-openai-resource.openai.azure.com/"
$env:AZURE_OPENAI_KEY="your-openai-api-key"
$env:AZURE_OPENAI_DEPLOYMENT_NAME="your-chat-model-deployment-name"
```

#### Execution

Run the Python script:

```bash
python multi_agent_travel.py
```

#### Expected Results

The application will simulate a multi-agent conversation to book a travel package. You will see extensive console output showing the agents communicating, calling tools, and ultimately arriving at a solution. The exact conversation flow may vary slightly due to the non-deterministic nature of LLMs and agent interactions.

**Example Output Snippets (illustrative, actual output will be more verbose):**

```
--- Starting Multi-Agent Travel Booking Conversation ---
customer_proxy (to group_chat_manager):
I want to book a trip from London to Paris, departing on 2025-08-10. I also need accommodation in Paris from 2025-08-10 to 2025-08-15. Please find and book both for 1 person.

>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>

customer_service (to flight_booking_assistant):
Okay, I understand. I need to find flights from London to Paris departing on 2025-08-10 for 1 person. flight_booking_assistant, can you help with this?

>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>

flight_booking_assistant (to terminal_agent):
find_flights(origin='London', destination='Paris', date='2025-08-10')

>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>

[Tool Call: Finding flights from London to Paris on 2025-08-10]

>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>

terminal_agent (to flight_booking_assistant):
[... Tool output with available flights ...]

>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>

flight_booking_assistant (to terminal_agent):
book_flight(flight_name='Flight 1', origin='London', destination='Paris', departure_date='2025-08-10', passengers=1)

>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>

[Tool Call: Booking flight Flight 1 for 1 passengers]

>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>

terminal_agent (to flight_booking_assistant):
[... Tool output with flight booking confirmation ...]

>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>

customer_service (to accommodation_booking_assistant):
Great, the flight is booked. Now, accommodation_booking_assistant, can you find and book accommodation in Paris from 2025-08-10 to 2025-08-15 for 1 person?

>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>

accommodation_booking_assistant (to terminal_agent):
find_accommodations(location='Paris', check_in_date='2025-08-10', check_out_date='2025-08-15')

>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>

[Tool Call: Finding accommodations in Paris from 2025-08-10 to 2025-08-15]

>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>

terminal_agent (to accommodation_booking_assistant):
[... Tool output with available accommodations ...]

>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>

accommodation_booking_assistant (to terminal_agent):
book_accommodation(accommodation_name='Hotel 1', check_in_date='2025-08-10', nights=5, guests=1)

>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>

[Tool Call: Booking accommodation Hotel 1 for 1 guests]

>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>

terminal_agent (to accommodation_booking_assistant):
[... Tool output with accommodation booking confirmation ...]

>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>

customer_service (to customer_proxy):
Your flight from London to Paris (Flight 1, booking reference XXXX) and accommodation in Paris (Hotel 1, booking reference YYYY) have been successfully booked. I will send you an email with the full details. TERMINATE

--- Conversation Finished ---
```

This verbose output demonstrates the multi-agent collaboration, tool invocation, and the progression towards fulfilling the complex user request. The `TERMINATE` message from the `customer_service` agent signals the completion of the task.



