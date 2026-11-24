::: {align="center"}
```{=html}
<!-- Animated title banner -->
```
`<a href="https://github.com/">`{=html}
`<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=700&size=30&pause=1000&color=39D5FF&center=true&vCenter=true&width=760&lines=NOVA;Non-Obsolete+Virtual+Assistant;Your+Intelligence.+Your+Control." alt="NOVA animated title" />`{=html}
`</a>`{=html}

`<br/>`{=html}

**A personal AI assistant for Windows --- designed to think, assist,
automate, and adapt.**

`<br/>`{=html}

![Platform](https://img.shields.io/badge/Platform-Windows%2011-0078D4?style=for-the-badge&logo=windows&logoColor=white)
![Status](https://img.shields.io/badge/Status-Early%20Development-FFB020?style=for-the-badge)
![License](https://img.shields.io/badge/License-TBD-808080?style=for-the-badge)

`<br/>`{=html}

*One assistant. Multiple models. Real tools. You stay in control.*
:::

------------------------------------------------------------------------

## ✨ What is NOVA?

**NOVA (Non-Obsolete Virtual Assistant)** is a Windows-first personal AI
assistant built to go beyond ordinary chat.

The goal is to create a secure, modular desktop assistant that can
understand requests, plan multi-step work, use approved tools, interact
with Windows applications, research the web, assist with coding, and
verify what it does.

NOVA is designed around a futuristic **2D energy ORB** that communicates
its state through motion and light --- idle, listening, thinking,
speaking, executing, success, and error.

> **NOVA --- Your Intelligence. Your Control.**

## 🚀 Vision and capabilities

  -----------------------------------------------------------------------
  Area                                Planned capabilities
  ----------------------------------- -----------------------------------
  AI brain                            Cloud and local models, model
                                      routing, streaming responses,
                                      provider fallbacks

  Desktop assistant                   Floating ORB, dashboard, system
                                      tray, notifications, keyboard
                                      shortcuts

  Voice                               Push-to-talk, wake word,
                                      speech-to-text, text-to-speech,
                                      interruptible speech

  Windows control                     App launching, file navigation,
                                      system diagnostics, approved
                                      automation

  Browser agent                       Web research, page extraction,
                                      browser workflows, downloads

  Agentic workflows                   Planning, tool selection,
                                      execution, verification, retries,
                                      background tasks

  Memory                              Searchable conversations, project
                                      memory, preferences, editable
                                      long-term memory

  Screen intelligence                 On-demand screen understanding and
                                      optional, visible live awareness

  Extensibility                       Plugins, custom skills, tool
                                      registry, permission controls

  Safety                              Risk-based approvals, audit logs,
                                      credential protection, emergency
                                      stop

  Reliability                         Testing dashboard, diagnostics,
                                      encrypted backups, recovery
                                      workflows
  -----------------------------------------------------------------------

*These are project goals, not a claim that every feature is already
implemented. See the roadmap for current development stages.*

## 🧠 How NOVA is designed

NOVA uses a modular desktop architecture. The frontend presents the
experience, the Python backend coordinates intelligence and tools, and a
centralized permission layer governs actions.

``` mermaid
flowchart TD
    U[User: Voice / Text] --> UI[Desktop UI · Tauri + React]
    UI <-->|Typed API / WebSocket| API[Python Backend · FastAPI]
    API --> ORCH[Task Orchestrator]
    ORCH --> ROUTER[AI Model Router]
    ROUTER --> CLOUD[Cloud Models · OpenRouter]
    ROUTER --> LOCAL[Local Models · Ollama / llama.cpp]
    ORCH --> AGENTS[Specialized Agents]
    AGENTS --> TOOLS[Controlled Tool Registry]
    TOOLS --> WIN[Windows Automation]
    TOOLS --> WEB[Browser Automation]
    TOOLS --> FILES[File Operations]
    ORCH <--> MEM[Memory · SQLite]
    SEC[Permission & Security Layer] -. governs .-> ORCH
    SEC -. governs .-> TOOLS
```

### Core engineering principles

-   **Modular by design:** clear boundaries between UI, backend, AI
    providers, agents, memory, and tools.
-   **Secure by default:** tools receive only the permissions they need.
-   **Human control:** consequential actions require confirmation.
-   **Verifiable execution:** NOVA should report what actually happened,
    not pretend a task succeeded.
-   **Local-first where practical:** private data and supported
    workloads can remain on the machine.
-   **Resource-aware:** local model selection must account for available
    RAM and GPU VRAM.

## 🧰 Technology stack

### Desktop application

  -----------------------------------------------------------------------------------
  Technology                                      Role
  ----------------------------------------------- -----------------------------------
  [Tauri 2](https://tauri.app/)                   Lightweight native desktop shell

  [React](https://react.dev/)                     Component-based user interface

  [TypeScript](https://www.typescriptlang.org/)   Type-safe frontend development

  [Tailwind CSS](https://tailwindcss.com/)        UI styling and design system

  [Framer Motion](https://motion.dev/)            Interface and ORB motion

  [Zustand](https://zustand.docs.pmnd.rs/)        Frontend state management

  Canvas / SVG                                    Animated 2D energy ORB and visual
                                                  effects
  -----------------------------------------------------------------------------------

### Backend and AI

  ----------------------------------------------------------------------------------------
  Technology                                           Role
  ---------------------------------------------------- -----------------------------------
  [Python 3.12+](https://www.python.org/)              Backend and automation runtime

  [FastAPI](https://fastapi.tiangolo.com/)             Backend API and WebSocket services

  [Pydantic](https://docs.pydantic.dev/)               Data validation and typed schemas

  AsyncIO                                              Asynchronous task execution

  [OpenRouter](https://openrouter.ai/)                 Initial cloud AI gateway

  [LiteLLM](https://docs.litellm.ai/)                  Provider abstraction and model
                                                       routing

  [Ollama](https://ollama.com/)                        Local model runtime

  [llama.cpp](https://github.com/ggml-org/llama.cpp)   Local inference support
  ----------------------------------------------------------------------------------------

### Automation, voice, and data

  -------------------------------------------------------------------------------------------------
  Technology                                                    Role
  ------------------------------------------------------------- -----------------------------------
  [Playwright](https://playwright.dev/)                         Browser automation

  PyAutoGUI / Pywinauto                                         Desktop interaction where
                                                                appropriate

  Windows UI Automation / PowerShell                            Native Windows control

  [Faster-Whisper](https://github.com/SYSTRAN/faster-whisper)   Speech recognition

  [Silero VAD](https://github.com/snakers4/silero-vad)          Voice activity detection

  [Piper](https://github.com/rhasspy/piper)                     Local text-to-speech

  SQLite / SQLCipher                                            Structured and encrypted local data

  SQLite FTS5                                                   Full-text memory and history search
  -------------------------------------------------------------------------------------------------

### Quality and delivery

  --------------------------------------------------------------------------
  Technology                             Role
  -------------------------------------- -----------------------------------
  [Pytest](https://pytest.org/)          Backend tests

  [Ruff](https://docs.astral.sh/ruff/)   Python linting and formatting

  [Git](https://git-scm.com/) /          Version control
  [GitHub](https://github.com/)          

  [Docker](https://www.docker.com/)      Optional isolated development
                                         services

  GitHub Actions                         CI workflows

  Windows installer tooling              Packaging and distribution
  --------------------------------------------------------------------------

> The stack is the intended architecture. Dependencies will be added as
> each feature is implemented and validated; not every listed technology
> is necessarily present in the repository yet.

## 🖥️ Target development machine

NOVA is being designed with this development environment in mind:

  Component          Target
  ------------------ ----------------------------------------
  OS                 Windows 11
  CPU                Intel Core i7-13620H
  Memory             16 GB DDR5
  GPU                NVIDIA RTX 4060 Laptop GPU · 8 GB VRAM
  Internal storage   512 GB SSD
  External storage   500 GB portable HDD

Local AI workloads will use appropriately quantized models and
hardware-aware settings. The external HDD is intended primarily for
backups and archives, rather than active model inference.

## 🗺️ Development roadmap

``` mermaid
flowchart LR
    A["01 · Foundation"] --> B["02 · AI Brain"]
    B --> C["03 · Computer Control"]
    C --> D["04 · Memory & Voice"]
    D --> E["05 · Agentic Intelligence"]
    E --> F["06 · Advanced Capabilities"]
    F --> G["07 · Security & Delivery"]
```

  -----------------------------------------------------------------------
  Phase                   Scope                   Status
  ----------------------- ----------------------- -----------------------
  01                      Tauri shell, React UI,  Planned / starting
                          FastAPI backend, ORB,   
                          app communication       

  02                      OpenRouter, model       Planned
                          selection, streaming    
                          chat, provider          
                          abstraction             

  03                      Windows app and file    Planned
                          control, browser        
                          automation, permissions 

  04                      Conversation memory,    Planned
                          long-term memory, voice 
                          pipeline                

  05                      Planner, executor,      Planned
                          specialized agents,     
                          verification            

  06                      Screen intelligence,    Planned
                          plugins, proactive      
                          tools, offline          
                          workflows               

  07                      Security hardening,     Planned
                          test suite, installer,  
                          documentation           
  -----------------------------------------------------------------------

Progress should be updated only when a phase has been implemented and
tested.

## 🔐 Security model

NOVA is intended to operate through a controlled tool system --- not
unrestricted access to the computer.

-   **Least privilege:** each tool and agent receives only the
    permissions it needs.
-   **Risk-based approval:** low-risk reversible tasks may run
    automatically; medium-risk tasks use configurable checkpoints;
    high-impact actions require explicit approval.
-   **Sensitive actions:** destructive operations, administrative
    changes, purchases, and external messages must not happen silently.
-   **Secret handling:** API keys belong in secure local storage, never
    in frontend code, source control, or logs.
-   **Privacy controls:** screen awareness is opt-in, visibly indicated,
    and configurable by application.
-   **Auditability:** record meaningful tool actions while avoiding
    unnecessary sensitive data.
-   **Emergency stop:** provide a clear way to stop active execution.

External webpages, downloaded files, and third-party plugins must be
treated as untrusted input.

## ⚙️ Configuration notes

### OpenRouter

OpenRouter is the initial cloud model gateway. Configure the API key
locally through NOVA's secure credential setup once that feature is
implemented.

**Never commit API keys or paste them into source files.** Keep local
environment files out of version control and provide a safe example
configuration containing placeholders only.

Example placeholder:

``` env
# Example only — never put a real key in a committed file.
OPENROUTER_API_KEY=your_key_here
```

The application should keep secrets in a secure local credential store
rather than relying on a frontend-accessible environment variable.

## 🧪 Testing philosophy

NOVA should test real capabilities through the same execution engine
used for normal tasks.

Planned test groups:

-   Basic Windows operations: launch apps, create and save a test file,
    navigate folders.
-   File navigation: search, inspect metadata, and read supported
    documents.
-   Browser workflows: open a page, search, extract content, and
    download a test file.
-   Multi-step tasks: plan, execute, verify, and recover from safe
    failures.
-   Reliability: permission checks, API failures, offline behavior, and
    resource usage.

Tests should run in a dedicated sandbox/workspace and must not use
personal files for destructive operations. A feature is not complete
until its relevant tests pass.

## 🏁 Getting started

NOVA is at the early development stage. Setup instructions will be
expanded as the initial application scaffold is implemented.

### Intended prerequisites

-   Windows 11
-   Git
-   Node.js LTS
-   Python 3.12+
-   Rust toolchain (for Tauri)
-   Tauri system prerequisites for Windows
-   An OpenRouter account/API key for cloud model testing (optional
    until AI integration)

### Planned first-run workflow

1.  Clone the repository.
2.  Install frontend dependencies.
3.  Create and activate a Python virtual environment.
4.  Install backend dependencies.
5.  Configure local secrets securely.
6.  Start the backend and desktop development app.
7.  Run the test suite.

Exact commands will be added after the project scaffold and dependency
files are created. Do not assume these steps are currently runnable.

## 📁 Intended repository structure

``` text
NOVA/
├── apps/
│   └── desktop/              # Tauri + React application
├── backend/
│   ├── api/                  # FastAPI routes and WebSockets
│   ├── core/                 # Configuration and application core
│   ├── ai/                   # Providers and model routing
│   ├── agents/               # Planner and specialized agents
│   ├── tools/                # Permission-controlled tools
│   ├── memory/               # Conversation and long-term memory
│   ├── security/             # Permissions, approvals, audit
│   └── tests/                # Backend tests
├── docs/                     # Architecture and development docs
├── scripts/                  # Development and build helpers
├── .gitignore
└── README.md
```

This is the intended structure; adapt it to the existing repository
rather than overwriting working files.

## 🤝 Development guidelines

-   Build incrementally, phase by phase.
-   Inspect the repository before changing it.
-   Preserve working code and user data.
-   Prefer real integrations over placeholder interactions.
-   Keep interfaces typed and validate inputs.
-   Add tests for important functionality.
-   Document setup, configuration, limitations, and security decisions.
-   Run builds and tests after meaningful changes.
-   Never report a feature as complete unless it has been verified.

## 📌 Project status

**NOVA is under active development planning / initial implementation.**
The architecture and intended capabilities are defined, but features
should be considered incomplete until they exist in the codebase and
pass tests.

------------------------------------------------------------------------

::: {align="center"}
### ✦ NOVA

**Non-Obsolete Virtual Assistant**

*Your Intelligence. Your Control.*

`<sub>`{=html}Built to assist. Designed to adapt. Engineered to keep you
in control.`</sub>`{=html}
:::
