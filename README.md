# automationgroups
A non-profit organization for collaborating on agentic Moqui app development, sales and maintenance.

# Automation Groups International (AGI) 🌐

_Building a rugged, event-driven, enterprise-grade AI automation fabric natively embedded inside the Moqui Ecosystem._

---

## The Vision

Automation Groups International (AGI) is a commercial, humanitarian, and open-source initiative dedicated to transforming enterprise software development and business operations through **agentic AI workflows**. 

Instead of relying on fragile, multi-process network sidecars (Python scripts, Node.js proxies, or local port tunnels) that are disconnected from enterprise business data, AGI embeds advanced Large Language Model (LLM) orchestration **in-process, straight inside the Java Virtual Machine (JVM) memory space**.

By bringing the AI brain into the exact same application layer as the data model, AGI enables autonomous agents to securely refactor code repositories, inspect system architectures, and drive interactive frontend canvases at the speed of local RAM.

---

## Architectural Philosophy

AGI is explicitly designed to eliminate the "accidental complexity" of modern AI integrations. The platform is structured around a three-tier unified architecture:

┌────────────────────────────────────────────────────────────────────────┐
│                   AGI Visual Canvas (Vue 3 / Quasar 2)                 │
│   - Multi-channel screen state repainting via streaming JSON tokens    │
└───────────────────────────────────▲────────────────────────────────────┘
│  (Native WebSockets)
┌───────────────────────────────────▼────────────────────────────────────┐
│                    AGI AI Extension Layer (agi-ai)                     │
│   - RxJava 3 Flowable Event Loop subscriber pipelines                  │
│   - Dynamic workspace/code crawlers & schema generation tools          │
└───────────────────────────────────▲────────────────────────────────────┘
│  (In-Process Lifecycle Bindings)
┌───────────────────────────────────▼────────────────────────────────────┐
│                Google Agent Development Kit (moqui-adk)               │
│   - Official Google ADK Java SDK & Session state runner                │
│   - Native JSR-380 / @Schema reflection engine                         │
└────────────────────────────────────────────────────────────────────────┘

1. **The Core Engine Layer (`moqui-adk`):** We strictly embrace the official **Google Agent Development Kit (ADK) Java SDK**, natively embedded as a standard Moqui component. This provides a rugged, database-driven configuration layer (`moqui.adk.AdkAgentConfig`) and bulletproof session execution management without external process drift.
2. **The Automation Extension Layer (`agi-ai`):** A decoupled extension component that hooks into the ADK startup lifecycle. It replaces static tool definitions with dynamic, metadata-driven workspace explorers (such as native XML screen interpreters like `get_artifact`) and structures them on-the-fly for Google Gemini's function-calling engine.
3. **The Reactive Transport Layer:** Direct, thread-safe WebSocket connections (`/agi-ws/{channel}`) that subscribe asynchronously to the ADK's underlying RxJava 3 `Flowable<Event>` emission streams. Text chunks and visual layout payload matrices are captured mid-flight and broadcasted instantly to the user interface.

---

## Core Capabilities

### 🛠️ In-Process Code Crafting & Refactoring
AGI exposes tools directly to the AI model that can programmatically traverse the local disk using Moqui's native component locations framework (`ec.factory.getComponentBaseLocations()`). The model can securely inspect structural entity data models, analyze layout configurations, map out modifications, and write back clean code changes without ever triggering a network serialization hop.

### 🎨 Human-In-The-Loop Canvas Orchestration
Unlike traditional chat bots that simply stream text blocks back to a scrolling log window, AGI structures tool outputs into deterministic JSON layout graphs. The frontend **Vue 3 / Quasar 2** canvas interprets these live structures to visually repaint the user interface in real time, giving the human operator seamless preview, modification, and veto power over the agent's actions before changes are committed.

### 🔒 Enterprise-Grade Security
By executing all operations inside the JVM, sensitive secrets (such as the `GEMINI_API_KEY` and internal database encryption contexts) never leak into external process spaces or browser contexts. Authentication and channel tokens are synchronized out of an isolated runtime hierarchy, satisfying rigid enterprise security boundaries by design.

---

## Open-Source Collaboration & Roadmap

We believe that the future of enterprise software is agentic, and the Moqui ecosystem provides the absolute best object-relational data mapping, service-oriented architecture, and multi-tenant security foundation on the market to support it.

Our immediate engineering path focuses on:
- **Dynamic Tool Registries:** Automatically reflecting Moqui Service Facade input parameters into standard JSON-Schema blocks that are fed to the LLM context on connection handshakes.
- **Visual Blueprint Trees:** Refining the JSON blueprint graph outputs so that complex screens can be broken down, localized, and dynamically reassembled by the model.
- **Clustered Scalability:** Utilizing Moqui’s native containerization and horizontal scaling structures to scale out multi-threaded agent execution runners seamlessly.

We are actively seeking to collaborate with fellow Moqui developers, system architects, and open-source contributors who want to move past loose scripting and build the definitive enterprise AI automation standard.

---

Developed by **Automation Groups International (AGI)**.  
_Public Domain under CC0 1.0 Universal — Built to augment the human experience._
