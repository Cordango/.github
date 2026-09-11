<img width="1299" height="321" alt="Cordango" src="https://github.com/user-attachments/assets/1105b1d8-d7a4-4232-b67e-d7504942f615" />

<p align="center">
  <img width="600" height="130" alt="Cordango" src="https://github.com/user-attachments/assets/4b41f0e3-1bde-42ee-a058-04b5ad9c849c" />
</p>

<p align="center">
  <strong>A new architecture for AI-generated business software</strong>
</p>

<p align="center">
  Define the application once. Run it on Cordango or compile it into conventional source code you own.
</p>

---

Cordango is an application platform built around a simple idea:

**the maintained artifact of a business application does not have to be its source code.**

Instead, a Cordango App Definition describes what the application *is*:

- entities and relationships
- permissions and roles
- processes and commands
- workflows and events
- calculations and rollups
- pages, forms and application UI

A deterministic compiler handles the repeatable implementation.

```text
Human / AI agent
       │
       ▼
 App Definition
       │
       ├──────────────► Cordango Platform
       │
       └──────────────► deterministic compiler
                              │
                              ▼
                       conventional source
```

## One definition, two destinations

### Run it on Cordango

Cordango Platform runs applications on a shared company foundation.

Apps can share things like **People, Organizations and Calendar**, reference records across applications, and react to events emitted by other apps instead of rebuilding the same company data in every tool.

```text
Purchase Requests ──approved──► Budget Tracker
        │
        └──────────────────────► Vendor Management

PTO ───────────────────────────► Resource Planning
```

The applications remain separate. They just understand the same company.

### Compile it to source

The same App Definition can be compiled into a conventional standalone application.

The current `dotnet-vue` target generates:

```text
ASP.NET Core
EF Core
PostgreSQL
Vue 3
Vuetify
Docker
```

The generated project belongs to you.

No Cordango account.
No licence server.
No model API.
No phone home.

The small standalone runtime can be referenced as a pinned NuGet package or embedded into the generated project.

Delete the Cordango toolchain afterwards and the application still builds.

## One app, three interfaces

A generated application isn't just a web UI.

The same application model is exposed to:

```text
Humans      → UI
Software    → REST / OpenAPI
AI agents   → MCP
```

The interfaces share the same underlying entities, commands and permission model.

That means a command such as `approve_claim` is the same business action whether somebody clicks a button, calls the API or invokes it through MCP.

## Deterministic where it should be

AI is very good at reasoning about what an application should do.

It does not need to reinvent authentication, persistence, API structure, migrations, permission plumbing and framework conventions every time.

Cordango separates those jobs:

> **The model describes the application. The compiler writes the repeatable parts.**

Given the same App Definition, generator version and scaffold version, Cordango produces the same generated files byte for byte.

That does not make a bad definition correct.

It makes its implementation reproducible.

## Built for humans and agents

Cordango source is intentionally much smaller than the implementation it represents.

For example, an application can define its own presentation and theme without describing Vuetify components or CSS:

```yaml
app: expenses
name: Expenses
version: 1.0.0

presentation:
  icon: credit-card-outline
  color: '#ea580c'
  category: Finance
  tagline: Claims, approvals, reimbursement

theme:
  primaryColor: '#ea580c'
  secondaryColor: '#f97316'
  font: Inter
  radius: medium
  density: comfortable
```

Entities, roles, processes, pages and workflows live in their own semantic source files.

Across five applications we measured, authoring the App Definition instead of generating the complete implementation required **90.6% to 98.4% fewer output tokens**.

That saving is a consequence of the architecture, not the architecture itself.

## More than CRUD

The current application language includes things such as:

- processes and guarded domain commands
- workflows and scheduled automation
- computed fields and dependency graphs
- rollups and windowed calculations
- ordered series with previous-row calculations
- tables, boards, calendars, timelines and Gantt views
- charts, dashboards, forms and configurable intake
- field-level permissions
- application events and cross-app subscriptions
- shared company records
- themes and application presentation

The [`examples`](https://github.com/Cordango/examples) repository contains complete applications ranging from a one-entity expense approval app to a 16-entity financial planning application, plus connected Finance, People and Operations suites.

## The open foundation

The application format, compiler, validator, CLI and standalone source generator are developed in the open under Apache-2.0.

The hosted Cordango Platform builds on that foundation with the shared runtime, company-wide data model, governance and cross-application capabilities.

Calling the entire Cordango platform open source would be a stretch.

The boundary is simpler:

**open toolchain, proprietary platform.**

## Start here

**[cordango/cordango](https://github.com/Cordango/cordango)**  
The application language, compiler, CLI and standalone generator.

**[cordango/examples](https://github.com/Cordango/examples)**  
Complete applications and connected multi-app suites.

**[Documentation](https://docs.cordango.com)**  
Concepts, authoring, CLI, MCP and deployment.

**[Quickstart](https://docs.cordango.com/quickstart)**  
From zero to a running generated application.

**[Cordango Platform](https://www.cordango.com)**  
The hosted company application platform.

---

Cordango is still **pre-alpha**. The language is moving, rough edges exist, and today `dotnet-vue` is the first complete generator target.

If application languages, compilers, AI-assisted development, internal tools or making business software considerably less ridiculous sound interesting, have a look around.

And say hi to Dante.

<img width="680" height="581" alt="Dante" src="https://github.com/user-attachments/assets/be0ff18e-f48a-40de-8736-d43f5378ac8b" />
