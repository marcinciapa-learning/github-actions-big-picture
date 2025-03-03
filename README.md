# GitHub Actions: The Big Picture Pluralsight course

Code for [GitHub Actions: The Big Picture](https://app.pluralsight.com/library/courses/github-actions-big-picture/table-of-contents) Pluralsight course

# What I learned
- A lot of actions, categorised, ready for reuse are available in GitHub marketplace.
- GitHub hosted distributed runners are available. It's also possible to use self-hosted runners in own environment.
- GitHub Workflows contain of Jobs, which by default run in parallel. Jobs contain of steps, individual actions which
make up a job.
- It's recommended to always specify versions of used GitHub action in step. Latest is used by default, which can
break your actions after an update.
- With `run` step it's possible to run command line command.
- `needs` keyword ensures that jobs run in a sequential order.
- Jobs are independent and common steps need to be repeated in every job. It ensure elasticity and changing
configuration between two different jobs.
- GitHub Settings->Environments for a repository allows configuring deployable environment on GitHub Pages.
- `permissions` section of a job configures what our workflow is allowed to do with the repository.
- If an action needs to write to repository, it needs to use GitHub Token, an environment secret, which is
available for every action (`secrets.GITHUB_TOKEN`). Combined with permissions, it allows performing allowed
operations.
