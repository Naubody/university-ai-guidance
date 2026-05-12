# Recommendations for using agentic AI
Agentic AI tools can take actions on your behalf, such as reading files, writing code, running terminal commands, browsing the web, or interacting with software. This makes them powerful, but also risky (see my [colloquium slides on agentic AI](https://drive.google.com/file/d/1PhEJvINEbkH8sZNFmFPrX3VnIoDQBDC0/view?usp=sharing)). Before using such tools in university work, please review the following recommendations. 
_Matthias Nau_

## What is an agentic AI?
Agentic AI refers to artificial intelligence systems designed to act autonomously or semi-autonomously to achieve specific goals. Unlike standard LLMs that merely answer questions or generate text, agentic AI can interact with its environment (e.g., executing code, using software, browsing the internet, and manipulating files), to complete complex, multi-step tasks.

## Recommendations

### 1.	Inform yourself about AI safety risks before use
Read up on the specific risks of agentic AI systems, especially when they are allowed to use tools, execute code, access files, browse the web, or interact with other software.


o	Read: [Careful adoption of agentic AI services](https://www.cyber.gov.au/business-government/secure-design/artificial-intelligence/careful-adoption-of-agentic-ai-services)

o	Read: [AI Agent Security Cheat Sheet (OWASP)](https://cheatsheetseries.owasp.org/cheatsheets/AI_Agent_Security_Cheat_Sheet.html)

### 2.	Learn about prompt injection
Prompt injections are attacks that cause an AI system to ignore your instructions, leak information, run unsafe commands, or take harmful actions based on malicious text found in websites, emails, documents, repositories, or other external content. Be especially careful when an agentic AI system reads webpages, emails, PDFs, GitHub repositories, shared documents, or downloaded files. External content may contain hidden or explicit instructions designed to manipulate the model.
o	Read: [LLM Prompt Injection Prevention Cheat Sheet (OWASP)](https://cheatsheetseries.owasp.org/cheatsheets/LLM_Prompt_Injection_Prevention_Cheat_Sheet.html)

### 3.	Beware of institutional-scale damage
Even without deliberate prompt injection attacks, AI systems have already caused serious damage to institutions when used carelessly or with excessive autonomy. Consider the recent case where an AI system permanently deleted a firm's internal database due to a misunderstood objective. These risks are not hypothetical.
o	Read Guardian article: [Claude AI deletes firm database
](https://www.theguardian.com/technology/2026/apr/29/claude-ai-deletes-firm-database)

### 4.	Inform your supervisor or project lead
Let your supervisor, PI, manager, or project lead know when you are using agentic AI tools for university-related work. This is especially important for research projects, teaching materials, or administrative work.

### 5.	Do not connect agentic AI to institutional systems
Do not connect agentic AI tools to university email, shared drives, student information systems, HR systems, finance systems, research databases, learning management systems, or internal networks unless this has been explicitly approved.

### 6.	Do not use OpenClaw
The use of OpenClaw (or similar aggressively autonomous, unverified open-source agents) is prohibited on university equipment, as it lacks standard safety rails and is known to execute high-risk terminal commands without user confirmation.

### 7.	Report incidents or near misses 
If you witness that an AI tool accesses something it should not have accessed, that it deleted or changed important files, leaks information, sends unintended messages, or behaves in other ways suspiciously, report it to your supervisor and/or the VU data security services at [ADD EMAIL]. Report such cases even if the issue was resolved to protocol the event, prevent others from making the same mistakes, and help increase expertise in our department over time.

### 8.	Do not give models access to sensitive data
Never provide agentic AI tools with access to confidential, personal, or institutionally sensitive data, including student data and research data. Do not give AI models access to the server or computing cluster.

### 9.	Never let an AI analyze your data directly
Instead of uploading raw data, use AI tools to help write the analysis scripts (using dummy or synthetic data), and run those scripts locally yourself.

### 10.	Never provide credentials or tokens
Never paste passwords, API keys, SSH keys, access tokens, recovery codes, or private certificates into an AI system. Avoid allowing agentic tools to access files or environments where such secrets may be stored.

### 11.	Use sandboxing
Run agentic AI tools only in a restricted environment, such as a sandbox, container, virtual machine, or other isolated workspace. For example, use terminal sandboxing features where available, such as in Antigravity.

### 12.	Use a separate device
Ideally, use a separate computer for agentic AI experimentation, especially when testing new or unfamiliar tools. Avoid using your primary work machine, especially if you already foresee risks.

### 13.	Apply the principle of least privilege
Never give the model full access to your machine, file system, browser, email, cloud storage, institutional accounts, or command line. Grant only the minimum access needed for the specific task at hand.

### 14.	Enforce boundaries at the system level, not the prompt level
Do not rely on natural language instructions to keep an agent safe (e.g., prompting the model with "Never delete a file"). Natural language boundaries are easily bypassed by the model's own hallucinations or external prompt injections. Instead, enforce boundaries at the infrastructure level. If you don't want the agent to delete files, run it in an environment where it physically lacks write/delete permissions.

### 15.	Maintain backups and use version control whenever possible
Always keep backups of your files before using agentic AI tools. This is especially important before allowing a model to edit, move, rename, generate, overwrite, or delete files. For code, documents, data-processing scripts, and configuration files, use version control such as Git. This approach will allow you to recover files that an AI agent changed or deleted outside your control.

### 16.	Keep the human in control 
Do not allow the model to execute high-impact actions without review. Require confirmation before deleting files, modifying important documents, installing software, sending emails, publishing content, submitting forms, changing permissions, or contacting external services.

### 17.	Avoid autonomous long-running tasks
Do not let an agent run unattended for extended periods, especially if it has file-system, network, browser, terminal, or account access. Monitor what it is doing and stop it if it behaves unexpectedly.

### 18.	Review outputs carefully
Do not assume that the model’s output is correct, safe, legal, or ethical. Check code, citations, calculations, summaries, data transformations, and generated text thoroughly before relying on them. Never trust AI-generated content blindly.

### 19. Remember that you remain fully responsible and accountable for harm caused by your AI agents
