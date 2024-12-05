---
title: Overview
layout: default
nav_order: 1
---
# Required Software and Services
{: .no_toc}
# Table of Contents
{: .no_toc .text-delta}
1. TOC
{:toc}

# Introduction

In this course, you'll be building your own Generative AI-powered application, and to do that effectively, we'll be using a set of powerful command-line interface (CLI) tools. While it might seem a bit intimidating at first, 
you'll quickly gain proficiency with practice. 

**Why the Command Line?**

You might be wondering, "Why not just use a graphical user interface (GUI)?" While GUIs are user-friendly for basic tasks, the CLI offers several advantages, especially when working with generative AI:

* **Precision and Control:** The CLI gives you fine-grained control over every aspect of your project, from managing code and dependencies to interacting directly with AI models.
* **Automation and Efficiency:** You can automate repetitive tasks, saving you time and effort. Imagine training a model with a single command or deploying your application to the cloud with ease.
* **Enhanced Collaboration:** The CLI makes it easier to share your work with others and collaborate on complex projects using version control systems like Git.
* **Unlocking AI Assistance:** Generative AI tools like Gemini, GitHub Copilot, and ChatGPT are particularly effective at assisting with CLI commands. They can help you you write commands, code, debug errors, and even suggest new approaches.

**Your CLI Arsenal**

Throughout this course, you'll become familiar with a range of powerful CLI tools:

* **Terminal and Shell:** Your gateway to the command line, providing a text-based interface to interact with your computer.
* **uv:** A modern tool for managing Python programming language based projects and their dependencies.
* **Git:** A version control system that allows you to track changes to your code, collaborate with others, and revert to previous versions if needed.
* **GitHub:** A platform for collaboration, managing projects, and hosting your code. Its CLI client `gh` allows for minimal context-switching and better productivity.
* **Google Cloud Platform (GCP):**  A suite of cloud computing services. Its CLI tool `gcloud` enables you to manage GCP resources from the command line.
* **Visual Studio Code:** A code editor with powerful CLI integration, enhancing your development workflow.
* **Starship:** A cross-shell prompt that provides a visually appealing and informative command-line experience.

**Connecting the Dots**

These CLI tools form the foundation for building, managing, and deploying your generative AI applications. You'll use them to:

* **Set up your development environment.**
* **Write and execute Python code.**
* **Manage project dependencies.**
* **Deploy and access AI models.**
* **Collaborate with teammates.**
* **Deploy your application to the cloud.**

Even if you're new to the command line, don't worry! This module will support your journey from getting started to gaining proficiency. 

# Terminal and Shell 
A terminal program (also known as a terminal emulator or command-line interface) is a text-based window that allows you to interact directly with your computer's operating system by typing commands. It's a powerful tool for managing files, running programs, and configuring system settings.

Here's how to access the terminal on different operating systems:

* **Windows:** Search for "Windows Terminal" in the Start Menu. If it is not pre-installed on your computer follow instructions from [➡️ here](https://learn.microsoft.com/en-us/windows/terminal/install)
* **macOS:** Open the "Terminal" application found in the Utilities folder within Applications.
* **Chrome OS:** Open the terminal application by searching for "Terminal" in the launcher.

A shell is a program that interprets the commands you type in a terminal and sends them to the computer's operating system to execute. It acts like a middleman between you and the computer, allowing you to control your system using text commands.

While often used interchangeably, a shell is different from a terminal:

* **Terminal:** The terminal is the window where you type commands. It's the visual interface.
* **Shell:** The shell is the program running *inside* the terminal that interprets those commands. It's the engine under the hood.

Here are the default shells in different operating systems:

* **macOS:** Zsh (Z shell)
* **Windows:** PowerShell
* **Chrome OS:** crosh (Chrome Shell)
* **Linux:** Bash (Bourne Again Shell)

This course primarily uses the Bash shell. While Zsh is also common, the differences won't significantly impact your learning. If your default shell isn't Bash or Zsh, follow the instructions below to ensure compatibility with typical cloud environments and AI/ML workflows.


{: .new-title}
> To-do
>
> If you are on Windows, enable Windows Subsystem for Linux (WSL) to install a Linux distribution like Ubuntu using instructions [➡️ here](https://learn.microsoft.com/en-us/windows/wsl/install). 
>
> If you are on Chrome OS, follow instructions from [➡️ here](https://support.google.com/chromebook/answer/9145439) to enable Linux and access Bash from Terminal.

# Git
Imagine Git as a time machine for your code, but with superpowers! Instead of saving countless versions of your files like "my_app_v1," "my_app_final," "my_app_really_final," Git tracks every single change you make. 

This is incredibly helpful in this course where you'll be constantly experimenting with AI prompts, model settings, and user interface designs. If a change causes problems, you can easily "rewind" to a previous, working version. Think of it as an "undo" button with infinite levels!

But Git does more than just version control:

* **Collaboration:** Git helps you seamlessly work with others on the same codebase. Everyone can contribute their changes without overwriting each other's work. This is crucial for your group projects!
* **Progress Tracking:**  You'll be showcasing your project weekly. With Git, you can "tag" each week's release, making it easy to compare and contrast your progress over time.  This also helps me (your instructor) track individual contributions and provide feedback.

Essentially, Git acts as a safety net, allowing you to experiment freely, collaborate effectively, and showcase your progress, all while ensuring your application remains operational despite rapid changes.

{: .new-title }
> To-do
>
>**Installing Git**
>
> 1. **Check for Git:** Open your terminal and type `git --version`. If Git is already installed, you'll see its version number.
> 1. **Install if needed:** If Git isn't installed, download it from the official website [➡️ here](https://git-scm.com/downloads) and follow the installation instructions for your operating system.

# uv
Imagine you're baking a cake. You wouldn't just throw all the ingredients together without measuring, right?  `uv` helps you do the same for your Python projects. It ensures you have the right "ingredients" (Python packages) and the right "amounts" (versions) so your code works correctly every time.

Why is this important?

* **Smoother Deployment:** In this course, you'll often deploy your project code to a cloud service and share it with your peers. uv ensures that your code runs smoothly across different environments by managing your project's dependencies and creating a reproducible Python setup. This simplifies the deployment process and helps your code work reliably wherever it's executed.
* **Consistency:**  Just like different flour brands can affect your cake, different Python package versions can affect your code. `uv` helps you avoid unexpected surprises.
* **Sharing:** If you share your "recipe" (code) with someone else, `uv` makes sure they can recreate it perfectly.
* **Future-proofing:** Even if Python changes in the future, your project will still work because `uv` keeps track of everything it needs.

Think of `uv` as a recipe book and ingredient list for your Python projects, keeping everything organized and consistent.

{: .new-title }
> To-do
>
> **Installing `uv`**
> To install `uv`, follow these simple steps:
> 1. **macOS/Linux:** Visit the official documentation [➡️ here](https://docs.astral.sh/uv/getting-started/installation/) and follow the instructions.
> 1. **Windows:**  Use your Bash shell within WSL and follow the Linux installation instructions from the link above.

# Visual Studio Code
While you might be familiar with Jupyter notebooks, in this course, we'll be using Visual Studio Code (VS Code) as our primary code editor. VS Code is a versatile and powerful tool that goes beyond basic code editing, offering features that enhance your workflow and productivity, especially when working with generative AI.

Here's why we recommend VS Code:

* **Extensible and Customizable:** VS Code has a rich ecosystem of extensions that allow you to tailor it to your specific needs. Think of extensions like apps on your phone – they add new functionalities and supercharge your coding experience.
* **Integrated Terminal:** Access the command line directly within VS Code, eliminating the need to switch between windows. This streamlined workflow is essential for efficient development.
* **AI-Powered Assistance:** Leverage extensions like GCP Code Cloud, GCP Gemini code assist, or GitHub Copilot to get AI-powered code suggestions, completions, and even generate entire code blocks, boosting your productivity and learning.
* **Excellent for Python Development:** VS Code provides robust support for Python, including features like intelligent code completion, debugging, and integration with popular Python tools.

{: .new-title }
> To-do
>
> **Installing VS Code:**
>
> To install VS Code, follow these simple steps:
>
> 1. **Download:** Visit the official VS Code website [➡️ here](https://code.visualstudio.com/Download) and download the installer for your operating system.
> 1. **Install:** Run the downloaded installer and follow the on-screen instructions.

VS Code's flexibility and extensive features make it the ideal code editor for this course, enabling you to write, test, and manage your generative AI projects with ease.

# Github
GitHub is like a central hub for all things code. It's where you'll store your project's source code, collaborate with your teammates, and manage your project's development. Think of it as a combination of Google Drive (for storing code), a project management tool (for organizing tasks), and a social media platform (for developers to connect and share ideas).

In this course, you'll use GitHub to:

* **Store and manage your code:** Keep your code organized and accessible.
* **Collaborate with your team:** Work together on code, share ideas, and review each other's contributions.
* **Plan and track your work:**  Clearly define tasks, assign responsibilities, and monitor progress.
* **Showcase your contributions:** Demonstrate your individual contributions to the project.

GitHub provides a centralized and transparent platform for your project development, facilitating collaboration, organization, and progress tracking.

To get the most out of GitHub in this course, be sure to explore these key features:

* **Issues:** Use issues to track tasks, brainstorm ideas, and discuss solutions with your team.
* **Discussions:** Engage in conversations with your group and instructor, ask questions, and share insights.
* **Wikis:** Create a knowledge base for your project, documenting decisions, resources, and progress.
* **Pull Requests:**  Submit your code changes for review and merge them into the main project.
* **GitHub-Flavored Markdown:** Learn this simple markup language to format your text and code in issues, discussions, and wikis.

These GitHub features are designed to enhance your collaboration and project management. Explore how generative AI can assist you within these features – from brainstorming ideas and generating code to documenting your progress. This hands-on experience will demonstrate the power of AI assistants for task execution.

{: .new-title }
> To-do
>
>**Get Started with GitHub:**
>
>1. **Sign Up:** If you don't already have a GitHub account, create one [➡️ here](https://github.com/signup).
>1. **Embrace the CLI:**  While GitHub offers a web interface, we'll be primarily using the `gh` command-line tool. Why? Because the CLI offers greater flexibility, automation, and integrates seamlessly with AI-powered tools. Imagine generating code, managing tasks, and collaborating with your team, all from your terminal!
>1. **Install `gh`:**  Follow the instructions [➡️ here](https://github.com/cli/cli#installation) to install the GitHub CLI client on your system.

# Google Cloud Platform
Public clouds like Google Cloud Platform (GCP) provide essential resources for learning and working with generative AI:

* **Accessibility:**  You can access powerful hardware (GPUs/TPUs) and software tools without upfront investment.
* **Scalability:** Easily adjust your computing resources as your AI projects grow.
* **Pre-trained models:** Experiment with cutting-edge AI models readily available on the cloud.
* **Cost-effectiveness:** Pay only for the resources you use, making experimentation more affordable. 

By leveraging a public cloud, you gain hands-on experience with the infrastructure and tools used to develop and deploy real-world generative AI applications.

Think of the public cloud like renting access to powerful computers, storage, and software over the internet. Instead of buying and maintaining your own hardware, you can tap into these resources on-demand, similar to how you use Google Docs or Office 365 without managing the physical servers they run on.

In this course, we'll be using Google Cloud Platform (GCP), one of the leading public cloud providers. You'll leverage GCP's services to:

* **Build your AI application:** Use Vertex AI to access different foundational models, experiment with prompt design, try out generative AI orchestration, and more.
* **Host your application:** Deploy your application on Cloud Run, making it accessible to your peers for review and feedback.
* **Manage your cloud resources:** Utilize services like IAM for access control, billing management to track costs, and logging/monitoring to understand your application's performance and resource usage.

**Important Cloud Considerations:**

As you begin your generative AI and cloud journey, it's crucial to be mindful of:

* **Billing:** Cloud services are billed based on usage. Leaving resources running unnecessarily can lead to unexpected costs. Always remember to shut down or delete resources when you're not using them.
* **Security:** Protect your cloud account and data by following security best practices. Never share your API keys or account credentials publicly (including on GitHub) and ensure proper authentication for your applications and storage.

By understanding these core concepts and practicing responsible cloud usage, you'll be well-equipped to harness the power of GCP for your generative AI projects.

{: .new-title}
> To-do
>
>**Accessing Google Cloud Platform**
> 
> To get started with GCP, sign up for a free account:
> 
> 1. **Visit the GCP website:** Go to [cloud.google.com](https://cloud.google.com/).
> 1. **Sign up for a Free Trial:**  You'll receive $300 in credit to explore GCP's services. 
> 1. **Important Notes:**
>     * You'll need to provide billing information, but you won't be charged unless you exceed the free credits or continue using paid services after the trial.
>     * Be sure to set up budget alerts to avoid any unexpected charges.
>
> **Getting Started with `gcloud`**
> 
> The `gcloud` command-line tool lets you manage your Google Cloud resources. Here's how to get started:
> 
> 1. **Install the Google Cloud SDK:**  This includes the `gcloud` tool.  Follow the instructions [here](https://cloud.google.com/sdk/docs/install).
> 
> 1. **Initialize `gcloud`:** Open your terminal and run: 
>    ```bash
>    gcloud init
>    ```
>    Follow the prompts to link `gcloud` to your Google Cloud account.
> 
> 1. **Authorize `gcloud` (if needed):** If you're using `gcloud` on a new machine or have multiple Google accounts, you might need to authorize it. Run:
>    ```bash
>    gcloud auth login
>    ```
>    This will open a browser window for you to sign in to your Google Cloud account.
> 
> That's it! You're ready to use `gcloud` to interact with Google Cloud.


With your GCP account, you'll have access to the powerful tools and services you need to build and deploy your generative AI applications.



# Starship
Imagine having a heads-up display for your terminal, showing you all the essential information about your project at a glance. That's Starship! This powerful tool enhances your command-line experience by providing a customizable and informative prompt.

![screen shot of terminal with starship prompt](/assets/img/nerd-font-symbols.png)

{: .text-right .fs-3 }
**Image credit:** starship.rs 

Starship displays:

* **Location:**  Where you are in your file system.
* **Git Status:** Which branch you're on and if there are any uncommitted changes.
* **Cloud Connection:**  The cloud account you're using (e.g., GCP).
* **Configuration:** Key settings like your current cloud region.
* **Programming Language:** The version of Python or other languages used in your project.

With Starship, you'll always have the critical context for your project right in your terminal, making your workflow smoother and more efficient.

{: .new-title}
> To-do
>
>**Installing Starship**
>
>To install Starship🚀 and transform your terminal experience, follow the instructions on the official Starship website:
>
>[➡️ Install Starship](https://starship.rs/guide/) 
