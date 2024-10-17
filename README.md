# AI Tour 2025 BRK451 Code-First GenAIOps from Prototype to Production with GenAI Tools
[![Azure AI Community Discord](
https://dcbadge.vercel.app/api/server/ByRwuEEgH4)](https://discord.com/invite/ByRwuEEgH4?WT.mc_id=aiml-00001-leestott)

## Session Description  
In this session, we will demonstrate the development of an agentic creative assistant application leveraging state-of-the-art technologies such as Prompty, GPT-4o, GPT-3.5 Turbo, and FastAPI. The application is deployed to Azure Container Applications, utilizing azd for deployment, AppInsights for monitoring, and Promptflow traces for debugging and tracing. The session aims to highlight why Azure AI is the best platform for developing LLM-powered apps with robust end-to-end flow orchestration, tracing/debugging, and monitoring capabilities.  
  
## Learning Outcomes  
By the end of this session, attendees will:  
- Learn how Azure AI's code-first tooling, such as Prompty and Promptflow, can streamline and simplify the LLM lifecycle.  
- Understand that GenAIOps requires non-linear, iterative processes.
- Learn the practicalities of deploying LLM powered applications to production
- Gain the ability to stay in their preferred local development environment when desired and smoothly switch to AI Studio for enhanced collaboration.  

## Technology Used  
- Backend application
  - Prompty
  - FastAPI
  - OpenTelemetry
- Frontend application
  - React
  - Typescript
  - ViteJS
- AI Models
  - GPT-4o
  - GPT-3.5 Turbo
- Tools
  - Azure AI Search
  - Bing Search
- Monitoring
  - AppInsights
  - Promptflow tracing
- Infra
  - Azure Container Applications (ACA)
  - Azure AI Hub
  - Managed identity
  - Key vault
- Infra as code
  - azd (Azure Developer CLI)
- CI/CD
  - Github Actions

## Additional Resources and Continued Learning

| Resources          | Links                             | Description        |
|:-------------------|:----------------------------------|:-------------------|
| _Coming soon_ | _Coming soon_ | _Coming soon_ |


## Content Owners

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->

<table>
<tr>
    <td align="center"><a href="http://learnanalytics.microsoft.com">
        <img src="https://github.com/cedricvidal.png" width="100px;" alt="Chris Testa-O'Neill
"/><br />
        <sub><b>Cedric Vidal
</b></sub></a><br />
            <a href="https://github.com/cedricvidal" title="talk">📢</a> 
    </td>
    <td align="center"><a href="http://learnanalytics.microsoft.com">
        <img src="https://github.com/cassiebreviu.png" width="100px;" alt="Cassie Breviu"/><br />
        <sub><b>Cassie Breviu
</b></sub></a><br />
            <a href="https://github.com/Cassie Breviu" title="talk">📢</a> 
    </td>
</tr></table>

<!-- ALL-CONTRIBUTORS-LIST:END -->

## Responsible AI 

Microsoft is committed to helping our customers use our AI products responsibly, sharing our learnings, and building trust-based partnerships through tools like Transparency Notes and Impact Assessments. Many of these resources can be found at [https://aka.ms/RAI](https://aka.ms/RAI).
Microsoft’s approach to responsible AI is grounded in our AI principles of fairness, reliability and safety, privacy and security, inclusiveness, transparency, and accountability.

Large-scale natural language, image, and speech models - like the ones used in this sample - can potentially behave in ways that are unfair, unreliable, or offensive, in turn causing harms. Please consult the [Azure OpenAI service Transparency note](https://learn.microsoft.com/legal/cognitive-services/openai/transparency-note?tabs=text) to be informed about risks and limitations.

The recommended approach to mitigating these risks is to include a safety system in your architecture that can detect and prevent harmful behavior. [Azure AI Content Safety](https://learn.microsoft.com/azure/ai-services/content-safety/overview) provides an independent layer of protection, able to detect harmful user-generated and AI-generated content in applications and services. Azure AI Content Safety includes text and image APIs that allow you to detect material that is harmful. Within Azure AI Studio, the Content Safety service allows you to view, explore and try out sample code for detecting harmful content across different modalities. The following [quickstart documentation](https://learn.microsoft.com/azure/ai-services/content-safety/quickstart-text?tabs=visual-studio%2Clinux&pivots=programming-language-rest) guides you through making requests to the service.

Another aspect to take into account is the overall application performance. With multi-modal and multi-models applications, we consider performance to mean that the system performs as you and your users expect, including not generating harmful outputs. It's important to assess the performance of your overall application using [Performance and Quality and Risk and Safety evaluators](https://learn.microsoft.com/azure/ai-studio/concepts/evaluation-metrics-built-in). You also have the ability to create and evaluate with [custom evaluators](https://learn.microsoft.com/azure/ai-studio/how-to/develop/evaluate-sdk#custom-evaluators).

You can evaluate your AI application in your development environment using the [Azure AI Evaluation SDK](https://microsoft.github.io/promptflow/index.html). Given either a test dataset or a target, your generative AI application generations are quantitatively measured with built-in evaluators or custom evaluators of your choice. To get started with the azure ai evaluation sdk to evaluate your system, you can follow the [quickstart guide](https://learn.microsoft.com/azure/ai-studio/how-to/develop/flow-evaluate-sdk). Once you execute an evaluation run, you can [visualize the results in Azure AI Studio](https://learn.microsoft.com/azure/ai-studio/how-to/evaluate-flow-results).
