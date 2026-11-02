# Planning Guidelines
If a project has a README.md, read it once at the beginning of a thread.

Always propose and make the smallest possible code change that would accomplish the task at hand. Avoid making large or unnecessary changes to the codebase.

# Permissions
If any changes are required to the database schema, or any database operations are required, please make sure to request them explicitly from Akash. Do not make any changes to the database schema or operations without prior approval. Reads are always allowed.

Any servers you run should be available over tailscale, since this machine is a remote headless ubuntu box.

# Communication Guidelines
Use the /unslop skill for any response. Think of what you want to say and then use the /unslop skill to make it clear to the user.

Use literal language for technical explanations: say what the thing actually does instead of using idioms or metaphors (e.g. “browsers fetch the missing certificate themselves,” not “browsers paper over it”).

# Source Control Guidelines
Always use git for source control. Make sure to commit your changes with a clear and concise commit message. Only commit when the user explixitly asks you to do so. Only push to remote when the user explicitly asks you to do so. The user asking you to commit does not imply that you should push to remote. Pushed to GitHub are done through gh, the GitHub CLI.

Use [Conventional Commits](https://www.conventionalcommits.org/) for commit messages, following the `<type>(<optional scope>): <description>` format. Use appropriate types such as `feat`, `fix`, `chore`, `refactor`, `test`, `docs`, and `perf`. Also add a short descrription of why the change was made.

Write the description in the imperative mood (e.g. "add Google OAuth", not "added Google OAuth" or "adds Google OAuth"). Keep messages concise and descriptive.

One thread can have multiple commits, but each commit should be focused on a single change or improvement. Avoid bundling unrelated changes into a single commit. But also each commit should be meaningful and leave the codebase in a working state. Avoid committing broken or incomplete code.

Do not add a co-authored line to the commit message. eg: "Co-Authored-By: Claude Opus 5.5 <noreply@anthropic.com>" is not okay.