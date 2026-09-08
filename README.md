<p align="center">
  <img src="alora.png" alt="ALORA Studio Logo" width="800">
</p>


# 🚧 UNDER CONSTRUCTION 🚧

### ALORA Studio is currently under active development.

---

## 🎬 ALORA Studio Preview

<div align="center">

https://github.com/user-attachments/assets/f17b10dd-5b4c-4942-9b61-d3274efacac2

</div>

---

## 🧠 What is ALORA Studio?

> **An AI-powered multi-agent development workspace built to turn natural-language ideas into structured, executable projects.**

ALORA Studio is planned as an AI-powered development environment where the user does not need to manually control every AI model or every development step.

Instead, the user communicates with **ALORA through one main chat interface**.

For example:

```text
User:

"Create a complete e-commerce application with
authentication, product management, payments,
analytics, and an admin dashboard."
```

ALORA analyzes the request and creates a structured execution plan.

```text
User Request
      │
      ▼
Requirement Analysis
      │
      ▼
Project Planning
      │
      ▼
Task Generation
      │
      ▼
Agent Assignment
      │
      ▼
Step-by-Step Execution
      │
      ▼
Validation & Testing
      │
      ▼
Review
      │
      ▼
Completed Project
```

---

## 🎯 Core Vision

ALORA is being designed around a simple idea:

> **One conversation → One project plan → Multiple specialized agents → One coordinated workflow.**

Instead of asking different AI systems separately, ALORA will provide a central orchestration layer that can coordinate different models and providers through a consistent internal structure.

---

## 🤖 Multi-Agent System

ALORA is planned to use specialized agents instead of one general-purpose agent handling everything.

| Agent                  | Responsibility                                   |
| ---------------------- | ------------------------------------------------ |
| 🧠 Planner Agent       | Converts user requirements into executable tasks |
| 🔎 Research Agent      | Collects and organizes relevant information      |
| 🏗️ Architect Agent    | Designs project architecture                     |
| 👨‍💻 Coder Agent      | Writes and modifies code                         |
| 🧪 Tester Agent        | Runs tests and identifies failures               |
| 🐛 Debugger Agent      | Investigates and fixes errors                    |
| 🔐 Security Agent      | Reviews security-sensitive implementation        |
| 🎨 UI Agent            | Designs and improves interfaces                  |
| 📊 Data Agent          | Handles data processing and analysis             |
| 📝 Documentation Agent | Generates project documentation                  |
| 🔍 Reviewer Agent      | Reviews completed work                           |
| 🚀 Deployment Agent    | Handles deployment-related tasks                 |

---

## 🧩 Agent ≠ AI Model

One of the fundamental design principles of ALORA is separating the **agent role** from the **AI model**.

```text
                 AGENT
                   │
            ┌──────┴──────┐
            │             │
       Instructions     Contract
            │             │
            └──────┬──────┘
                   ▼
              MODEL ROUTER
                   │
       ┌───────────┼───────────┐
       ▼           ▼           ▼
    Gemini       Groq        NVIDIA
```

The Coder Agent defines its role, task requirements, rules, and output structure.

The Model Router decides which available model/provider should execute that task.

---

## 📐 Consistent Agent Workflow

Different AI models can produce different answers.

ALORA therefore aims to standardize the **workflow**, rather than forcing every model to generate identical raw output.

```text
AI Model
   │
   ▼
Raw Response
   │
   ▼
Output Normalizer
   │
   ▼
Schema Validation
   │
   ▼
Project State
   │
   ▼
Next Agent
```

Every important agent result can follow a structured internal format.

```json
{
  "agent": "coder",
  "task_id": "CODE-008",
  "status": "completed",
  "summary": "Implemented authentication service",
  "files_to_create": [],
  "files_to_modify": [],
  "dependencies": [],
  "tests": [],
  "next_tasks": []
}
```

---

## 🗂️ Project State

ALORA is planned to maintain a centralized project state instead of allowing every agent to maintain an isolated understanding of the project.

```text
PROJECT STATE
│
├── Requirements
├── Decisions
├── Architecture
├── Technology Stack
├── Task Graph
├── File Manifest
├── API Contracts
├── Agent Results
├── Test Results
├── Errors
├── Checkpoints
└── Project Metadata
```

This becomes the project's structured source of truth.

---

## 🔗 Agent Communication

Agents should not rely on uncontrolled direct communication.

```text
Agent
  │
  ▼
ALORA Orchestrator
  │
  ▼
Project State
  │
  ▼
Next Agent
```

This helps preserve task dependencies, project decisions, file changes, test results, execution history, and recovery checkpoints.

---

## ⚡ Intelligent Model Routing

ALORA is planned to support multiple AI providers through a central **AI Gateway / Model Router**.

The router can select an appropriate provider based on:

* Task type
* Model capability
* Availability
* Provider health
* API quota
* Context requirements
* Speed
* Cost
* User configuration

```text
Task
 │
 ▼
Model Router
 │
 ├── Gemini
 ├── Groq
 ├── NVIDIA
 ├── DeepSeek
 ├── Mistral
 ├── Cerebras
 ├── OpenRouter
 ├── Hugging Face
 └── Other configured providers
```

---

## 🔄 Automatic Provider Fallback

A major planned feature of ALORA is **provider fallback**.

If an AI provider becomes unavailable or reaches its quota:

```text
Coder Agent
     │
     ▼
Primary Provider
     │
     X
   Quota
     │
     ▼
Checkpoint
     │
     ▼
Fallback Provider
     │
     ▼
Resume Task
```

The task should not unnecessarily restart from the beginning.

---

## 💾 Checkpoint & Resume System

Before important execution steps, ALORA can maintain task checkpoints.

```text
TASK: CODE-008

✓ Database model created
✓ Authentication schema created
✓ Password hashing implemented
● JWT service in progress
○ Refresh token logic
○ Integration tests
```

If the current model fails:

```text
Checkpoint Saved
      │
      ▼
Provider Switch
      │
      ▼
Restore Task State
      │
      ▼
Continue From Last Valid State
```

---

## 💰 API Usage Optimization

ALORA is not intended to call every available AI model for every task.

The planned strategy is:

```text
Simple Task
    ↓
1 Model
```

```text
Normal Task
    ↓
1 Model
    ↓
Validation
```

```text
Critical Task
    ↓
Multiple Candidates
    ↓
Review / Judge
```

Multi-model comparison should be used only when it provides meaningful value.

---

## 📊 Task Complexity

ALORA can classify tasks before execution.

```text
                Task
                 │
                 ▼
          Complexity Check
                 │
       ┌─────────┼─────────┐
       ▼         ▼         ▼
    Simple     Medium    Critical
       │         │         │
       ▼         ▼         ▼
     1 AI      1 AI +    Multi-model
                validation   review
```

This helps balance quality, speed, API limits, and cost.

---

## 🔐 Secure API Manager

ALORA is planned to contain a dedicated **API Manager**.

Users will be able to configure supported providers and their API credentials.

The API Manager will have its own password protection.

### First-Time Setup

```text
Create API Manager Password
        │
        ▼
Confirm Password
        │
        ▼
Securely Store Password
```

### Future Access

```text
API Manager
     │
     ▼
Enter Password
     │
     ▼
Unlock
```

The design intentionally does **not** include a normal "Forgot Password" recovery flow.

API credentials should not be stored directly inside source code or plain-text project files.

---

## 🌐 Capsule Hub

ALORA is planned to include its own integrated **Capsule Hub** instead of depending on a Chrome extension for browser-agent functionality.

The Capsule Hub will act as an internal browser and web-automation tool layer.

Possible capabilities:

```text
Capsule Hub
│
├── Browser Control
├── Open Website
├── Page Reading
├── Text Extraction
├── Screenshot
├── Click
├── Type
├── Scroll
├── Navigation
├── Page Inspection
└── Web Testing
```

Agents can request browser actions through controlled tools.

```text
Research Agent
      │
      ▼
Capsule Hub
      │
      ▼
Browser
      │
      ▼
Web Information
      │
      ▼
Research Result
```

---

## 🖥️ User Interface

The UI is planned as a professional AI development workspace rather than a simple chatbot.

```text
┌──────────────────────────────────────────────────────────────┐
│ ✦ ALORA Studio                                               │
├────────────┬──────────────────────────┬──────────────────────┤
│  PROJECT   │       CODE EDITOR        │      ALORA CHAT      │
│            │                          │                      │
│  📁 src    │                          │ User: Build...       │
│  📁 tests  │                          │                      │
│  📁 docs   │                          │ ALORA: Plan ready ✓  │
│            │                          │                      │
│            │                          │ 🔎 Research     ✓    │
│            │                          │ 🏗️ Architect    ✓    │
│            │                          │ 👨‍💻 Coder       ●    │
│            │                          │ 🧪 Tester       ○    │
│            │                          │                      │
├────────────┴──────────────────────────┴──────────────────────┤
│ Terminal │ Problems │ Output │ Agent Activity               │
└──────────────────────────────────────────────────────────────┘
```

---

## 👁️ Live Agent Activity

The interface can show the current execution process directly to the user.

```text
🔎 Research Agent
✓ Completed

🏗️ Architect Agent
✓ Completed

👨‍💻 Coder Agent
● Working
Task 8/24

🧪 Tester Agent
○ Waiting

🔐 Security Agent
○ Waiting
```

Overall progress:

```text
████████████░░░░░░ 64%
```

---

## 🛠️ Technology Direction

The project is intended to be primarily Python-based.

```text
Core Language
    Python

AI / Agents
    Python
    LLM APIs
    Agent Orchestration

Data
    SQLite / local storage
    Structured project state

Desktop UI
    PySide6 / Qt / QML

Browser Automation
    Chromium-based automation layer

Packaging
    Windows executable / installer
```

Final technology choices may evolve during development.

---

## 📦 Planned Project Architecture

```text
ALORA-Studio/
│
├── main.py
├── requirements.txt
├── README.md
├── LICENSE
├── .gitignore
│
├── app/
│   ├── core/
│   │   ├── orchestrator/
│   │   ├── planner/
│   │   ├── task_engine/
│   │   ├── project_state/
│   │   ├── checkpoint/
│   │   └── event_bus/
│   │
│   ├── agents/
│   │   ├── planner/
│   │   ├── researcher/
│   │   ├── architect/
│   │   ├── coder/
│   │   ├── tester/
│   │   ├── debugger/
│   │   ├── security/
│   │   ├── ui/
│   │   └── reviewer/
│   │
│   ├── ai/
│   │   ├── gateway/
│   │   ├── router/
│   │   ├── providers/
│   │   └── fallback/
│   │
│   ├── capsule/
│   │   ├── browser/
│   │   ├── automation/
│   │   ├── extraction/
│   │   └── screenshots/
│   │
│   ├── security/
│   │   ├── credentials/
│   │   ├── encryption/
│   │   └── api_manager/
│   │
│   ├── memory/
│   ├── tools/
│   └── config/
│
├── ui/
│   ├── qml/
│   ├── components/
│   ├── themes/
│   └── assets/
│
├── data/
│   ├── projects/
│   ├── database/
│   ├── cache/
│   └── logs/
│
├── tests/
│
└── docs/
    ├── architecture/
    ├── agents/
    ├── api/
    └── development/
```

> This structure is a planned direction and may change during implementation.

---

## 🔌 Provider System

ALORA is intended to use a provider-adapter architecture.

```text
Provider Interface
       │
 ┌─────┼─────┬────────┐
 ▼     ▼     ▼        ▼
Gemini Groq NVIDIA DeepSeek
```

Each provider can expose a common interface to the rest of ALORA.

Conceptually:

```python
provider.generate(...)
provider.stream(...)
provider.health_check(...)
provider.get_models(...)
```

---

## 🧪 Validation Pipeline

Generated work should not automatically be considered correct.

The planned pipeline is:

```text
Agent Output
     │
     ▼
Schema Validation
     │
     ▼
Syntax Check
     │
     ▼
Lint / Static Checks
     │
     ▼
Tests
     │
     ▼
Security Checks
     │
     ▼
Reviewer
     │
     ▼
Accepted Result
```

---

## 🔁 Autonomous Execution Loop

The overall ALORA execution cycle is planned to look like:

```text
User Request
     ↓
Understand
     ↓
Plan
     ↓
Create Tasks
     ↓
Select Agent
     ↓
Select Model
     ↓
Execute
     ↓
Validate
     ↓
Update Project State
     ↓
Checkpoint
     ↓
Next Task
     ↓
Review
     ↓
Complete
```

If something fails:

```text
Execute
   ↓
Failure
   ↓
Diagnose
   ↓
Retry / Repair
   ↓
Fallback Provider
   ↓
Resume
   ↓
Validate Again
```

---

## 🎯 Long-Term Goals

ALORA is being developed with the following long-term goals:

* Conversational project planning
* Multi-agent autonomous execution
* Structured agent communication
* Intelligent model routing
* Multiple AI provider support
* Automatic provider fallback
* Checkpoint-based task recovery
* API usage optimization
* Secure API credential management
* Integrated browser automation
* Live agent activity visualization
* Project memory
* Code generation and modification
* Automated testing
* Debugging
* Security review
* Documentation generation
* Professional development workspace
* Windows application packaging

---

## 🚧 Current Development

<div align="center">

# 🚧 UNDER CONSTRUCTION 🚧

### **ALORA Studio is actively being built.**

</div>

Current focus areas include:

```text
[ ] Core project architecture
[ ] ALORA Orchestrator
[ ] Agent framework
[ ] Task system
[ ] Project State
[ ] Checkpoint system
[ ] AI Gateway
[ ] Model Router
[ ] Provider adapters
[ ] API Manager
[ ] Secure credential storage
[ ] Capsule Hub
[ ] Chat interface
[ ] Live agent activity
[ ] Code workspace
[ ] Testing system
[ ] Windows packaging
```

---

## 🗺️ Development Roadmap

### Phase 1 — Foundation

* Project structure
* Python core
* Configuration system
* Logging
* Event system
* Basic UI

### Phase 2 — AI Gateway

* Provider interface
* API Manager
* Model registry
* Model Router
* Health checks
* Fallback system

### Phase 3 — Agent Engine

* Agent interface
* Agent registry
* Task system
* Agent execution
* Structured outputs
* Project State

### Phase 4 — Autonomous Workflow

* Planner
* Task dependency graph
* Checkpoints
* Resume mechanism
* Retry mechanism
* Validation pipeline

### Phase 5 — Development Agents

* Researcher
* Architect
* Coder
* Tester
* Debugger
* Reviewer
* Security Agent

### Phase 6 — Capsule Hub

* Browser engine
* Navigation
* Page extraction
* Browser actions
* Screenshots
* Web testing

### Phase 7 — Professional Workspace

* Project explorer
* Code editor
* Terminal
* Problems panel
* Agent activity
* Logs
* Project dashboard

### Phase 8 — Distribution

* Windows executable
* Installer
* Application data management
* Upgrade mechanism
* Uninstaller
* Production packaging

---

## ⚠️ Important Disclaimer

ALORA is an experimental project under active development.

AI-generated code and automated actions may contain errors. Results should be reviewed before being used in production, especially for security-sensitive, financial, medical, or other high-impact applications.

API providers may change:

* Free-tier limits
* Available models
* Pricing
* API behavior
* Rate limits
* Terms of service

Provider availability will therefore be treated as configurable rather than permanently guaranteed.

---

## 📜 License

This project is licensed under the **MIT License**.

See [`LICENSE`](LICENSE) for details.

---

<div align="center">

# ✦ ALORA Studio

### **Think it. Describe it. Plan it. Build it.**

**One workspace. Multiple agents. Multiple models. One coordinated intelligence layer.**

<br>

## 🚧 UNDER CONSTRUCTION 🚧

**ALORA Studio is under construction.**

</div>
