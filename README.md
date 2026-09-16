# HELIX

**Autonomous Software Engineering Intelligence**

HELIX is an autonomous AI software engineering system that takes a software objective, analyzes the project, plans tasks, executes changes, runs tests, diagnoses failures, repairs the implementation, replans when necessary, and verifies the final result.

## Core Loop

```text
GOAL → UNDERSTAND → PLAN → SELECT MODEL → ACT → EXECUTE
→ OBSERVE → DIAGNOSE → REPAIR → RETEST → REPLAN → VERIFY
```

Unlike a conventional code-generation workflow, HELIX uses execution results and failures as feedback for subsequent decisions.

## Key Capabilities

* Project-aware code and structure analysis
* Dynamic task planning and dependency management
* Model selection with fallback handling
* Controlled file and execution tools
* Automated testing and failure diagnosis
* Iterative repair and retesting
* State persistence and execution history
* Checkpoint and recovery support
* Acceptance-criteria based verification
* Final project packaging and engineering report

## Architecture

```text
User Goal
   │
   ▼
Development Manager
   │
   ▼
Model Router
   │
   ▼
Tool Orchestrator
   ├── File Operations
   ├── Code Search
   ├── Execution
   └── Testing
   │
   ▼
Observation
   │
   ▼
Diagnosis / Repair
   │
   └──→ Replan
          │
          ▼
        Verify
```

## Models

HELIX uses a model-routing layer rather than a single fixed model. Gemini models provide the primary reasoning and coding layer, with fallback models available when a model becomes unavailable or reaches an API limit.

A local Qwen-based model can also serve as a resilience layer when suitable hardware is available.

## Execution

The current implementation is provided as a Google Colab notebook.

```text
HELIX.ipynb
```

The notebook can analyze a built-in demonstration project or work with an uploaded project within an isolated workspace.

## Outputs

A completed run can produce:

```text
project-final.zip
development_report.md
project_state.json
execution_log.json
```

These artifacts capture the resulting project, execution state, engineering changes, and verification results.

## Scope

The current implementation is optimized for Python projects and demonstrates autonomous software engineering through a closed-loop execution and feedback process.

## Future Extensions

Potential extensions include stronger multi-language support, richer code retrieval, improved checkpointing, additional model providers, and distributed execution.
