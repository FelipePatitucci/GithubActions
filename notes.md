Key Components:

Workflows

- Attached to a GitHub repository
- Contains 1 or more jobs
- Triggered by events

Jobs

- Contains 1 or more steps
- Runs on a specific runner (execution environment)
- Can be conditionally run
- Can be run in parallel (default) or sequentially

Steps

- Run a specific action (shell script, python script, etc)
- Can use custom or third-party actions
- Are executed sequentially
- Can be conditionally run

Events (Workflow Triggers)

- Repository Related
  - Push
  - Branch
  - Fork
  - Pull Request
    - Opened
    - Closed
    - Reopened
- Other
  - repository_dispatch (REST API request triggers workflow)
  - schedule (Cron)
  - workflow_dispatch (manullay triggered)
  - workflow_call (called by another workflow)

Actions: A custom application that performs a specific task

- Can be written in any language
- Can be published or requested from the GitHub Marketplace
- Can be used in a workflow

Expressions: A way to use get dynamic values of variables inside a workflow

- ${{}} is the Syntax for expressions
- Example: ${{ toJSON(github) }}
