# github-actions-demo

🔹 1. Environment Variables (env)
    What it does:
    Stores reusable values (like config, URLs, app names) that can be used across your workflow.

    Why it’s used:

    Avoid repeating values
    Centralize configuration
    Make workflows cleaner


🔹 2. Secrets
    What it does:
    Stores sensitive data securely (API keys, passwords, tokens).

    Why it’s used:

    Keeps credentials safe
    Prevents exposing secrets in code/logs
    Automatically masked in logs


🔹 3. Artifacts
    What it does:
    Stores files generated during a workflow so they can be used later or downloaded.

    Why it’s used:

    Share files between jobs
    Save build outputs (e.g., dist, logs)
    Debug failures by downloading logs/files


🔹 4. Cache Dependencies
    What it does:
    Saves dependencies (like npm packages) so they don’t need to be installed every time.

    Why it’s used:

    Speeds up workflows
    Reduces repeated downloads
    Improves CI performance


🔹 5. Services
    What it does:
    Runs additional containers (like databases) alongside your job.

    Why it’s used:

    Integration testing (DB, Redis, etc.)
    Simulate real application environment
    Test backend + DB together


🔹 6. Timeout
    What it does:
    Stops a job if it runs longer than a defined time.

    Why it’s used:

    Prevents stuck/infinite jobs
    Saves CI minutes/resources
    Improves reliability


🔹 7. Concurrency
    What it does:
    Controls how many workflow runs can execute at the same time.

    Why it’s used:

    Cancel old runs when new ones start
    Avoid duplicate deployments
    Ensure only latest code is deployed


🔹 8. Continue on Error
    What it does:
    Allows a step to fail without stopping the workflow.

    Why it’s used:

    Optional checks (like lint warnings)
    Non-critical steps
    Prevent full pipeline failure


🔹 9. Manual Trigger (workflow_dispatch)
    What it does:
    Allows you to run a workflow manually from GitHub UI.

    Why it’s used:

    Run deployments on demand
    Trigger jobs with custom inputs
    Useful for staging/production releases


🔹 10. Inputs (for manual/reusable workflows)
    What it does:
    Lets you pass dynamic values into workflows.

    Why it’s used:

    Make workflows reusable
    Customize behavior (env, version, region)
    Avoid hardcoding values


🔹 11. Job Dependencies (needs)
    What it does:
    Defines execution order between jobs.

    Why it’s used:

    Create pipelines (build → test → deploy)
    Ensure one job completes before another starts


🔹 12. Matrix Strategy
    What it does:
    Runs the same job multiple times with different configurations.

    Why it’s used:

    Test across multiple environments (Node versions, OS)
    Parallel execution
    Reduce duplicate code


🔹 13. If Conditions
    What it does:
    Controls when a job/step should run.

    Why it’s used:

    Run jobs only on specific branches/events
    Conditional deployments
    Skip unnecessary steps


🔹 14. Jobs vs Steps
    What it does:

    Job: A full unit of work (runs on a runner)
    Step: A task inside a job

    Why it’s used:

    Organize workflows logically
    Separate concerns (build/test/deploy)


🔹 15. Parallel vs Sequential Execution
    What it does:

    Parallel → jobs run at same time
    Sequential → jobs wait for others

    Why it’s used:

    Speed (parallel)
    Control flow (sequential)


🔹 16. Docker Usage in GitHub Actions
    What it does:
    Runs jobs inside containers or builds Docker images.

    Why it’s used:

    Consistent environment
    Easy deployment
    Matches production setup


🔹 17. Reusable Workflows
    What it does:
    Allows one workflow to call another.

    Why it’s used:

    Avoid duplication
    Standardize CI/CD processes
    Share logic across projects


🔹 18. Outputs
    What it does:
    Pass data from one job/step to another.

    Why it’s used:

    Share dynamic values (version, build info)
    Connect jobs in pipeline


🔹 19. Scheduling (Cron)
    What it does:
    Runs workflows automatically at specific times.

    Why it’s used:

    Nightly builds/tests
    Maintenance jobs
    Automation without manual trigger