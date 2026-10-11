<img width="1299" height="321" alt="Cordango" src="https://github.com/user-attachments/assets/1105b1d8-d7a4-4232-b67e-d7504942f615" />

# Cordango

**Let AI figure out what to build. Let a compiler handle the boring parts.**

We've got some pretty good AI coding tools now. Yet we still ask them to write the same authentication, CRUD, API endpoints, forms and permission checks over and over again.

Why?

Cordango takes a different approach. Let your Agent describe a business application in YAML, yes...all of it, entities, rules, permissions, ui..the whole app! Then compile it into an actual application.

And save token along the way. 

## What we're building

There are two sides to Cordango.

### The open-source developer tools

The [Cordango CLI and compiler](https://github.com/cordango/cordango) take an App Definition and generate a full-stack application. The current generators target .NET + Vue and Node + Vue, with some features still missing from the Node target.

You don't need a Cordango account. You don't need our hosting. You can generate the project, take the code and do whatever you want with it.

This is the part we're developing in the open under Apache 2.0.

### The hosted platform

[Cordango Cloud](https://cordango.com) is for teams who'd rather run apps than manage them. Apps can work with shared People and Organizations, along with common permissions and other platform services.

It's a separate product, not a requirement for using the compiler.

## Try the compiler

If you have the .NET SDK installed:

```sh
dotnet tool install -g Cordango.Cli

cordango new expenses
cd expenses
cordango check
cordango configure
cordango build

cd generated/expenses
docker compose up --build
```

Open `http://localhost:8080` and create your admin account.

Prefer Homebrew, Scoop or a standalone binary? The [installation guide](https://docs.cordango.com/cli/install) has the options.

## Where to go

| | |
| --- | --- |
| [cordango/cordango](https://github.com/cordango/cordango) | CLI, application language, validator and source generators |
| [cordango/examples](https://github.com/cordango/examples) | Actual application definitions, not just a todo app |
| [Documentation](https://docs.cordango.com) | Installation, concepts, authoring and CLI reference |
| [Building with AI](https://docs.cordango.com/ai/overview) | Using Claude Code or another agent with Cordango |
| [Cordango Cloud](https://cordango.com) | The hosted business app platform |

## Early days

We're still early, and the format is evolving. There are rough edges and things we haven't figured out yet.

If you're building internal tools, experimenting with AI-generated software, or just think writing the same boilerplate for the hundredth time is getting a little ridiculous, have a look.

Found something broken? [Open an issue](https://github.com/cordango/cordango/issues). Have a different idea for how this should work? [Start a discussion](https://github.com/cordango/cordango/discussions).

We'd rather hear what's wrong than pretend it's all finished.
