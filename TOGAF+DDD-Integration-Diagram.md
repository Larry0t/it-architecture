## TOGAF + DDD: Integration Diagram

```asci
|---------------------------------------------------------------|
|                 Architecture Vision / Phase A                 |
|                                                               |
|   • Business Goals / Strategy                                 |
|   • High-Level Capability Map                                 |
|   • Domain Exploration (Event Storming, Subdomains)           |
|---------------------------------------------------------------|
                      |
                      v
|---------------------------------------------------------------|
|                 Business Architecture / Phase B               |
|                                                               |
|   • Business Capability Map                                   |
|   • Business Processes                                        |
|   • **DDD: Identify Bounded Contexts**                        |
|   • **DDD: Define Ubiquitous Language**                       |
|---------------------------------------------------------------|
                      |
                      v
|---------------------------------------------------------------|
|     Information / Application Architecture / Phase C          |
|                                                               |
|   • TOGAF Data Architecture                                   |
|   • TOGAF Application Services                                |
|   • **DDD: Context Maps** (e.g., Shared Kernel, ACL, Customer/Supplier) |
|   • **DDD: Define Aggregates, Entities, Value Objects**       |
|   • **DDD: Define Context APIs / Domain Events**              |
|---------------------------------------------------------------|
                      |
                      v
|---------------------------------------------------------------|
|       Technology Architecture / Phase D                       |
|                                                               |
|   • Technology Stack                                          |
|   • Infrastructure / Platform Architecture                    |
|   • Deployment Topology                                       |
|   • **DDD: Map Contexts to Runtime (microservices, modules)** |
|   • **DDD: Define Integration via Events / Anti-Corruption**  |
|---------------------------------------------------------------|
                      |
                      v
|---------------------------------------------------------------|
|        Migration, Implementation & Change (Phases E–H)        |
|                                                               |
|   • Roadmap & Transition Architectures                        |
|   • Governance (TOGAF)                                        |
|   • **DDD: Incremental Migration of Bounded Contexts**        |
|   • **DDD: Evolve Context Maps and Aggregates Over Time**     |
|---------------------------------------------------------------|
```

## 🔍 Explanation of Key Parts

### 1. Top Layer (Vision / Phase A)
   - Use TOGAF to set strategic direction (capabilities, stakeholder goals).
   - Use DDD’s Event Storming or similar to explore domain complexity and identify subdomains.

### 2. Business Architecture (Phase B)
   - Build a Capability Map (TOGAF) to understand business capabilities.
   - Identify bounded contexts (DDD) and define the ubiquitous language for each context.

### 3. Information / Application Architecture (Phase C)
   - Use TOGAF to define data models and application components.
   - Use DDD to model domain inside each bounded context: define aggregates, entities, and value objects.
   - Map interactions between bounded contexts (Context Maps), including anti-corruption layers, shared kernels, or conformist relationships.
   - Define domain APIs (commands, queries) and domain events.

### 4. Technology Architecture (Phase D)
   - Choose platforms, infrastructure, deployment topology using TOGAF.
   - Align bounded contexts to runtime architecture (e.g., microservices, modular apps).
   - Design integration using DDD patterns: event-driven communication, anti-corruption layers, context translation.

### 5. Migration & Governance (Phases E–H)
   - Plan migrations in TOGAF: transition architectures, roadmap, work packages.
   - Incrementally migrate bounded contexts (especially core domain) using DDD principles.
   - Use TOGAF governance alongside DDD decision records.
   - Over time, evolve the bounded contexts, adjust context maps, and refactor aggregates as the domain model matures.

⸻
