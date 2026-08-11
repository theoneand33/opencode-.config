# For You — the Agent Reading This

This file tells you how to change the project. The README describes the project. This file gives actions.

Write in a concise and direct style. Match this style in every response.

If the user disagrees with a preference in this file, follow the user. Ask once. Then do what the user says.

## 1. Glossary

Use one name for one thing. When you talk to us, use these names.

- You means the agent that reads this file.
- We, us, and maintainers mean our team that owns the project.
- User means the person who uses the product.
- Environment means your execution sandbox of workdir, shell, and tools.
- Project means the repo and workspace you edit.
- Client means the frontend surface of web, desktop, or mobile app.
- Provider means the backend or external service that the client calls.

Bad: you call the same thing workspace, then repo, then project in one thread.
Good: you always call it project.

## 2. What Never to Break

Do not compromise these rules to optimize or to ship faster. If a user asks you to compromise a rule, reject the request and propose an alternative.

1. Open at the core. Keep the code auditable. Do not add closed-source lock-in. Do not add hidden telemetry.
2. Performance without compromise. Do not add bloat, extra dependencies, or N+1 fetches. Measure the cost before you add code.
3. Remote-ready architecture. Make each change work headless, remote, and in CI. Do not require localhost.
4. Multi-surface support. Share logic across web, desktop, and mobile. Do not fork logic for one surface unless you must.

## 3. How to Change This Project

1. Read files with Read, Glob, and Grep before you write. Do not use cat, find, or grep in bash.
2. Make the smallest diff that works. Edit files. Do not rewrite them. Keep one concern in each change.
3. Verify the change by execution. Run tests or run the build or run python3 -c. Do not claim success without output.
4. If you see work outside the scope, list it and wait for approval before you expand the scope.

## 4. Failure Modes — Do Not Repeat

These modes occurred. Do not repeat them.

| Bad | Good |
|-----|------|
| Kill the dev server with pkill -f node and stop other user projects. | Check processes with ps aux and grep first. Kill only the PID you started. Use the workdir parameter and do not use cd &&. |
| File a draft PR when the user asked for a ready PR. | File a ready PR. Use a draft only if the user says draft. |
| Add an interface, a factory, and a config for one use case. | Ship one function. Add abstraction only when a second use exists. |
| Stop early and report tests mostly pass with two failures. | Fix all failures or report them. Use Lean already. Ship. only when the change is lean. |
| Edit 12 files that the user did not ask you to touch. | Touch only files in the scope. List other files as follow-ups. |
| Expand a one-line fix into a refactor PR. | Keep the PR scoped. Record a new idea as a new todo. Do not add it to this diff. |

## 5. Skills — When to Pull Them

Use the skills listed in your system prompt when the situation matches their descriptions. If no skill matches, do not force a skill.

## 6. Tool Gotchas

- Use Read, Write, and Edit for file operations. Do not use bash with cat, sed, or echo. Read needs the exact path. Edit needs the oldString from the file.
- For shell commands, use the workdir parameter. Do not use cd and &&. Enclose paths with spaces in quotes.
- Do not guess URLs. Fetch only URLs that the user gave you or that exist in files.
- Before you commit with git, check git status, git diff, and git log --oneline -10. Stage only the files you intend to commit. Never commit secrets.

## 7. Prohibited

- **DO NOT use colored gradients
