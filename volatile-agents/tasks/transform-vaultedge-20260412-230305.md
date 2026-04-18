# Agent Task

## Agent Type
TRANSFORM

## Project Name
Vaultedge

## Target Project Path
/Users/avolatile/Desktop/Volatile Solutions/Agent Center/volatile-agents/target-projects/vaultedge-site

## Project Link / Repo
https://github.com/AVolatile/vaultedge-site.git

## Task Description
Open the project located at the target path and perform a full transformation using the transformation agent.

You must scan the actual project files and:
- infer the site's real industry or company type from the template
- replace placeholder, demo, or generic content with production-grade fictional business content that fits that industry
- remove template/origin traces from public content, metadata, comments, and project-authored code where appropriate
- keep the public site branding aligned to the fictional in-template business, not Volatile | Solutions
- preserve legitimate third-party dependency license text unless the dependency itself is removed or replaced
- ensure consistency across HTML, CSS, JS, metadata, and visible UI content

## Output Expectation
1. Real file-level edits must be made directly inside the Target Project Path
2. Create a result file at:
/Users/avolatile/Desktop/Volatile Solutions/Agent Center/volatile-agents/output/transform-vaultedge-20260412-230305-result.md

3. The result file must include:
- inferred industry and fictional business identity used
- list of files modified
- exact type of changes made per file
- any remaining areas requiring manual review

## Constraints
- Do NOT scan outside the Target Project Path
- Do NOT generate only a summary
- You must perform real edits first, then report
