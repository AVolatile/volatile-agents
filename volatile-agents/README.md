# volatile-agents

`volatile-agents` is a local runner workspace for transforming website templates into portfolio-ready, industry-correct example businesses that Volatile | Solutions can showcase.

## Workflow

1. Put a site folder inside `target-projects/` or pass `--repo-url` on the transform command.
2. Run `./transform <site>` from the `volatile-agents` folder.
3. The runner resolves the target project, writes a task file in `tasks/`, runs `codex exec` inside that project using the transformation agent contract, and writes a result file in `output/`.
4. The transformation rewrites template/demo content into a believable fictional business that matches the template's industry.
5. Add `--commit` or `--push` only when the target project is a git repo.

## Commands

`./transform vaultedge`

- Resolves `vaultedge` against folders inside `target-projects/`
- Creates a timestamped task file
- Runs the transformation agent in the target project
- Rewrites the template into a fictional business that matches the original niche
- Expects a timestamped result file in `output/`

`./transform vaultedge --repo-url https://github.com/AVolatile/vaultedge-site.git`

- Clones the repo into `target-projects/` first if it does not exist
- Then runs the same transformation flow

`./transform vaultedge --push`

- Runs the transformation flow
- Stages and commits target repo changes
- Pushes the current repo `HEAD` to `origin`

## Notes

- The runner only edits the selected project under `target-projects/`
- Public site branding should stay aligned to the template's inferred business type, not default to Volatile | Solutions
- The selected project only needs to be a git repo when `--commit` or `--push` is used
- The root workspace keeps the generated task and result files outside the site repo
- Use `./bin/volatile-agent help` for the full option list
