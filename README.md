# Ambience DevOps platform onboarding

This repository is the organization-owned entry point for enrolling repositories
in the Ambience DevOps platform. It contains the human review form only; the
canonical policy, workflow templates, and enforcement implementation live in
`ambience-Inc/devops-platform`.

Enrollment is deliberately staged:

1. Open an **Enroll repository in Ambience Platform** issue in this repository.
2. Select a workload profile and lifecycle stage, and link the target
   repository's manifest/caller pull request.
3. Pin that caller to the reviewed full 40-character devops-platform commit.
4. Run compatibility canaries before changing required checks or deployment
   ownership.
5. Move the repository to managed enforcement only after the Governance App
   source and protected configuration are verified.

The issue form does not enroll a repository, change settings, create secrets,
or grant a bypass. Repositories describe workload intent in
`.ambience/devops.yaml`; provider placement, capacity, credentials, and budgets
remain centrally controlled.

Do not activate organization rulesets until the Governance App, repository
custom properties, failing unconfigured-repository check, and one configured
canary have all been proven from their expected identities.
