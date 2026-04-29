# actionInAction

A minimal GitHub repository demonstrating **scheduled GitHub Actions workflows**.

## What it does

A workflow runs automatically every 5 minutes and prints the current UTC time followed by "Hello world" to the console:

```
2026-04-29T17:25:00 UTC Hello world
```

The workflow is defined in [`.github/workflows/hello-world.yml`](.github/workflows/hello-world.yml).

## How to verify the job runs

1. Open this repository on GitHub.
2. Click the **Actions** tab at the top of the repository.
3. In the left sidebar, click **Hello World** to filter by this workflow.
4. You will see a list of completed (and possibly running) workflow runs, each timestamped.

## How to see the console output

1. Click on any run in the list.
2. Click the **hello** job inside that run.
3. Expand the **Print Hello World with UTC time** step — you will see the output line, e.g.:

   ```
   2026-04-29T17:25:00 UTC Hello world
   ```

## Notes

- GitHub Actions scheduled workflows **may be delayed by 1–10 minutes** during periods of high load on GitHub's infrastructure. The cron `*/5 * * * *` means the job is *queued* every 5 minutes, but actual execution timing is best-effort.
- Scheduled workflows only run on the **default branch** (`main`).
