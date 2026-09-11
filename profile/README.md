<img width="1299" height="321" alt="image" src="https://github.com/user-attachments/assets/1105b1d8-d7a4-4232-b67e-d7504942f615" />

<p align="center"> <img width="600" height="130" alt="logo-white" src="https://github.com/user-attachments/assets/4b41f0e3-1bde-42ee-a058-04b5ad9c849c" /> </p>
  
 <p align="center"> <strong>Build anything. Run it like it belongs to the company.</strong> </p>


[Cordango](http://www.cordango.com "Cordango") is an AI-first application platform for building complete business applications on a shared, governed runtime.

Build anything. Run it like it belongs to the company.

Cordango is an application platform for building business software on a shared, governed company foundation.

Apps share identity, people, organizations, permissions, audit history and company context instead of creating another isolated database, login and copy of your business every time somebody builds something.

Underneath the platform is an open application format and deterministic compiler.

## Why?

AI has become very good at writing code.

But authentication, permissions, persistence, API structure and application plumbing do not need to be invented again every time an application is generated.

Cordango moves the maintained artifact up a level.

The human or agent describes **what the application is**. A deterministic compiler handles the implementation that should not vary between generations.

Given the same App Definition, generator version and scaffold version, Cordango produces the same application byte for byte.

That does not make a bad definition correct.

It makes the implementation reproducible.

## A tiny example

```yaml
entity: expense_claim

fields:
  submitted_by:
    type: reference
    targetEntity: person

  amount:
    type: money
    currency: EUR
    required: true
```

There is no SQL query, connection string, controller or component in that definition.

Those are implementation details produced from it.

cordango check
cordango build

The current dotnet-vue target generates a conventional application using ASP.NET Core, EF Core, PostgreSQL, Vue 3 and Vuetify.

generated/expenses/

├── api/

├── web/

├── Dockerfile

└── docker-compose.yml

Delete Cordango afterwards and the generated project still builds.

Built for humans and agents

The App Definition is intentionally much smaller than the implementation it represents.

That makes it practical for a human to review and practical for an AI agent to create and modify.

Across five applications we measured, writing the definition instead of generating the complete implementation avoided between 90.6% and 98.4% of output tokens.

That saving is a consequence of the architecture, not the architecture itself.

The model describes the application. The compiler writes the repeatable parts.


## Main Links
[Start here](https://docs.cordango.com/quickstart "Start here"): Want to get started quickly? Install the CLI and off ye go!

[cordango](http://github.com/cordango/cordango "Cordango/Cordango"): The main repository for our CLI, Code-Generator and Schema

[docs](http://docs.cordango.com "Documentation"): Documentation, concepts and guides
generators: Source generators for standalone applications

[examples](http://github.com/cordango/examples "examples"): Example Cordango applications


## What Cordango does
- Build complete business applications from structured app definitions
- Create apps with AI, YAML or JSON
- Share users, data and permissions across applications
- Run applications on a common governed runtime
- Define entities, views, workflows, calculations, hooks and more
- Validate applications before they run
- Generate standalone conventional source code from the same definition
- Keep your application portable instead of locking it inside a proprietary builder
- One application, two ways to run it

A Cordango application is defined independently from how it is deployed.

### Run it on Cordango

Use the Cordango platform and its shared runtime, company data, identity, permissions, integrations and governance.

###  Generate it as source code

Compile the same application into a standalone project using a supported generator and deploy it wherever you want.

The application stays the same. The deployment model is your choice.

## The open foundation

We're building the application definition, schema, compiler and source-generation tooling in the open.

The hosted Cordango platform builds on top of that foundation with the runtime and company-wide services needed to operate applications at scale.


More of the Cordango ecosystem will become public as it stabilizes.



Cordango is still early, expect bugs :)

If you're interested in application runtimes, deterministic code generation, AI-assisted development, low-code, no-code or just making business software considerably less ridiculous, you're in the right place.

Oh, and say hi to Dante!

<img width="680" height="581" alt="dante-blueprint" src="https://github.com/user-attachments/assets/be0ff18e-f48a-40de-8736-d43f5378ac8b" />
