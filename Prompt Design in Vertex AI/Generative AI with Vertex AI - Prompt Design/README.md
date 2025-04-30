# Prompt Design in Vertex AI - Google Gen AI

# Generative AI with Vertex AI: Prompt Design

# **GSP1151**

[](https://cdn.qwiklabs.com/GMOHykaqmlTHiqEeQXTySaMXYPHeIvaqa2qHEzw6Occ%3D)

# **Overview**

This lab explores prompt engineering and best practices for designing effective prompts to improve the quality of your LLM-generated responses. You'll learn how to craft prompts that are concise, specific, and well-defined, focusing on one task at a time. The lab also covers advanced techniques like turning generative tasks into classification tasks and using examples to enhance response quality. For further exploration, refer to the [official documentation on prompt design](https://cloud.google.com/vertex-ai/generative-ai/docs/learn/prompts/introduction-prompt-design).

# Gemini

[Gemini](https://deepmind.google/technologies/gemini/) is a family of powerful generative AI models developed by Google DeepMind, capable of understanding and generating various forms of content, including text, code, images, audio, and video.

### **Gemini API in Vertex AI**

The Gemini API in Vertex AI provides a unified interface for interacting with Gemini models. This allows developers to easily integrate these powerful AI capabilities into their applications. For the most up-to-date details and specific features of the latest versions, please refer to the official [Gemini documentation](https://cloud.google.com/vertex-ai/generative-ai/docs/learn/models#gemini-models).

### **Gemini Models**

- [**Gemini Pro**](https://deepmind.google/technologies/gemini/pro/): Designed for complex reasoning, including:
    - Analyzing and summarizing large amounts of information.
    - Sophisticated cross-modal reasoning (across text, code, images, etc.).
    - Effective problem-solving with complex codebases.
- [**Gemini Flash**](https://deepmind.google/technologies/gemini/flash/): Optimized for speed and efficiency, offering:
    - Sub-second response times and high throughput.
    - High quality at a lower cost for a wide range of tasks.
    - Enhanced multimodal capabilities, including improved spatial understanding, new output modalities (text, audio, images), and native tool use (Google Search, code execution, and third-party functions).

# Prerequisites

Before starting this lab, you should be familiar with:

- Basic Python programming.
- General API concepts.
- Running Python code in a Jupyter notebook on [Vertex AI Workbench](https://cloud.google.com/vertex-ai/docs/workbench/introduction).

# **Objectives**

In this lab, you will learn how to:

- Get started with prompt engineering using the Google Gen AI SDK.
- Apply best practices for prompt design, including conciseness, specificity, and task definition.
- Explore various text generation use cases with the Google Gen AI SDK, such as:
    - Ideation
    - Question answering
    - Text classification
    - Text extraction
    - Text summarization

# **Setup and requirements**

# Before you click the Start Lab button

Read these instructions. Labs are timed and you cannot pause them. The timer, which starts when you click **Start Lab**, shows how long Google Cloud resources are made available to you.

This hands-on lab lets you do the lab activities in a real cloud environment, not in a simulation or demo environment. It does so by giving you new, temporary credentials you use to sign in and access Google Cloud for the duration of the lab.

To complete this lab, you need:

- Access to a standard internet browser (Chrome browser recommended).

**Note:** Use an Incognito (recommended) or private browser window to run this lab. This prevents conflicts between your personal account and the student account, which may cause extra charges incurred to your personal account.

- Time to complete the lab—remember, once you start, you cannot pause a lab.

**Note:** Use only the student account for this lab. If you use a different Google Cloud account, you may incur charges to that account.

# How to start your lab and sign in to the Google Cloud console

1. Click the **Start Lab** button. If you need to pay for the lab, a dialog opens for you to select your payment method. On the left is the Lab Details pane with the following:
    - The Open Google Cloud console button
    - Time remaining
    - The temporary credentials that you must use for this lab
    - Other information, if needed, to step through this lab
2. Click **Open Google Cloud console** (or right-click and select **Open Link in Incognito Window** if you are running the Chrome browser).
    
    The lab spins up resources, and then opens another tab that shows the Sign in page.
    
    ***Tip:*** Arrange the tabs in separate windows, side-by-side.
    
    **Note:** If you see the **Choose an account** dialog, click **Use Another Account**.
    
3. If necessary, copy the **Username** below and paste it into the **Sign in** dialog.Copied!
    
    `"Username"`
    
    content_copy
    
    You can also find the Username in the Lab Details pane.
    
4. Click **Next**.
5. Copy the **Password** below and paste it into the **Welcome** dialog.Copied!
    
    `"Password"`
    
    content_copy
    
    You can also find the Password in the Lab Details pane.
    
6. Click **Next**.
    
    **Important:** You must use the credentials the lab provides you. Do not use your Google Cloud account credentials.
    
    **Note:** Using your own Google Cloud account for this lab may incur extra charges.
    
7. Click through the subsequent pages:
    - Accept the terms and conditions.
    - Do not add recovery options or two-factor authentication (because this is a temporary account).
    - Do not sign up for free trials.

After a few moments, the Google Cloud console opens in this tab.

**Note:** To access Google Cloud products and services, click the **Navigation menu** or type the service or product name in the **Search** field.

[](https://cdn.qwiklabs.com/9Fk8NYFp3quE9mF%2FilWF6%2FlXY9OUBi3UWtb2Ne4uXNU%3D)

# **Task 1. Open the notebook in Vertex AI Workbench**

1. In the Google Cloud console, on the **Navigation menu** (), click **Vertex AI > Workbench**.
    
    [](https://cdn.qwiklabs.com/tkgw1TDgj4Q%2BYKQUW4jUFd0O5OEKlUMBRYbhlCrF0WY%3D)
    
2. Find the `Workbench instance name` instance and click on the **Open JupyterLab** button.

The JupyterLab interface for your Workbench instance opens in a new browser tab.

# **Task 2. Set up the notebook**

1. Open the `notebook name` file.
2. In the **Select Kernel** dialog, choose **Python 3** from the list of available kernels.
3. Run through the **Getting Started** and the **Import libraries** sections of the notebook.
    - For **Project ID**, use `Project ID`, and for **Location**, use `Region`.

**Note:** You can skip any notebook cells that are noted *Colab only*. If you experience a 429 response from any of the notebook cell executions, wait 1 minute before running the cell again to proceed.

Click **Check my progress** to verify the objective.

Install packages and import libraries.

Check my progress

# **Task 3. Prompt engineering best practices**

Prompt engineering is all about how to design your prompts so that the response is what you were indeed hoping to see. The idea of using "unfancy" prompts is to minimize the noise in your prompt to reduce the possibility of the LLM misinterpreting the intent of the prompt. Below are a few guidelines on how to engineer "unfancy" prompts.

In this section, you'll cover the following best practices when engineering prompts:

- Be concise
- Be specific, and well-defined
- Ask one task at a time
- Improve response quality by including examples
- Turn generative tasks to classification tasks to improve safety
1. Run through the **Be concise** section of the notebook.

Click **Check my progress** to verify the objective.

Be concise.

Check my progress

1. Run through the **Be specific, and well-defined** section of the notebook.

Click **Check my progress** to verify the objective.

Be specific, and well-defined.

Check my progress

1. Run through the **Ask one task at a time** section of the notebook.

Click **Check my progress** to verify the objective.

Ask one task at a time.

Check my progress

1. Run through the **Watch out for hallucinations** section of the notebook.

Click **Check my progress** to verify the objective.

Watch out for hallucinations.

Check my progress

# **Task 4. Reduce Output Variability**

How can you attempt to reduce the chances of irrelevant responses and hallucinations? One way is to provide the LLM with [system instructions](https://cloud.google.com/vertex-ai/generative-ai/docs/multimodal/send-chat-prompts-gemini#system-instructions). In this section, you will see how system instructions works and how you can use them to reduce hallucinations or irrelevant questions for a travel chatbot.

1. Run through the **Using system instructions to guardrail the model from irrelevant responses** section of the notebook.

Click **Check my progress** to verify the objective.

Using system instructions to guardrail the model from irrelevant responses.

Check my progress

1. Run through the **Turn generative tasks into classification tasks to reduce output variability** section of the notebook.

Click **Check my progress** to verify the objective.

Generative tasks lead to higher output variability.

Check my progress

1. Run through the **Classification tasks reduces output variability** section of the notebook.

Click **Check my progress** to verify the objective.

Classification tasks reduces output variability.

Check my progress

# **Task 5. Improve Response Quality by Including Examples**

Another way to improve response quality is to add examples in your prompt. The LLM learns in-context from the examples on how to respond. Typically, one to five examples (shots) are enough to improve the quality of responses. Including too many examples can cause the model to over-fit the data and reduce the quality of responses.

Similar to classical model training, the quality and distribution of the examples is very important. Pick examples that are representative of the scenarios that you need the model to learn, and keep the distribution of the examples (e.g. number of examples per class in the case of classification) aligned with your actual distribution.

1. Run through the **Improve response quality by including examples** section of the notebook.

Click **Check my progress** to verify the objective.

Improve response quality by including examples.

Check my progress

# **Congratulations!**

Congratulations! In this lab you learned prompt engineering best practices using Generative AI with Google Gemini. You explored use cases which follow the best practices of being concise, specific, well-define, providing examples and asking one at a time when using LLMs to generate responses.

# Next steps / learn more

Check out the following resources to learn more about Gemini:

- [Gemini Overview](https://deepmind.google/technologies/gemini/)
- [Generative AI on Vertex AI Documentation](https://cloud.google.com/vertex-ai/docs/generative-ai/learn/overview)
- [Generative AI on YouTube](https://www.youtube.com/@googlecloudtech/)
- Explore the Vertex AI [Cookbook](https://cloud.google.com/vertex-ai/generative-ai/docs/cookbook) for a curated, searchable gallery of notebooks for Generative AI.
- Explore other notebooks and samples in the [Google Cloud Generative AI repository](https://github.com/GoogleCloudPlatform/generative-ai).

# Google Cloud training and certification

...helps you make the most of Google Cloud technologies. [Our classes](https://cloud.google.com/training) include technical skills and best practices to help you get up to speed quickly and continue your learning journey. We offer fundamental to advanced level training, with on-demand, live, and virtual options to suit your busy schedule. [Certifications](https://cloud.google.com/certification/) help you validate and prove your skill and expertise in Google Cloud technologies.

**Manual Last Updated February 12th, 2025**

**Lab Last Tested February 12th, 2025**

Copyright 2025 Google LLC All rights reserved. Google and the Google logo are trademarks of Google LLC. All other company and product names may be trademarks of the respective companies with which they are associated.