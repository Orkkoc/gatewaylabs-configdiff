# ConfigDiff

ConfigDiff is a configuration drift detection product focused on helping teams compare environments such as PROD, UAT, and TEST before drift becomes a release, reliability, or compliance problem.

This repository is the public companion repository for ConfigDiff. It is intentionally focused on three things:

- product overview
- public documentation
- sanitized examples

## Overview

Configuration drift usually starts small: a manual hotfix, an environment-specific override, or a release step that did not happen everywhere. Those differences often stay invisible until they become failed releases, production incidents, or audit pain.

ConfigDiff is intended to make that drift visible through baseline-aware comparisons, repeatable monitoring, reporting, alerts, and policy-driven checks.

## Who It Is For

ConfigDiff is primarily aimed at:

- DevOps, platform, and release teams managing multiple environments
- Microsoft-stack teams working with .NET, IIS, `appsettings.json`, and `web.config`
- Teams using Azure DevOps or similar CI/CD workflows
- Organizations operating hybrid, partially automated, or legacy environments

## What You Will Find Here

### Product Overview

- [Product overview](docs/product-overview.md)
- [How it works](docs/how-it-works.md)
- [Use cases](docs/use-cases.md)

### Docs

- [Docs index](docs/README.md)
- [Policy examples](docs/policy-examples.md)
- [Integration patterns](docs/integration-patterns.md)
- [Roadmap](ROADMAP.md)

### Examples

- [Demo seed example](examples/demo-seed/README.md)
- [Sample drift report](examples/sample-drift-report.md)

## Repository Scope

This is not the full private SaaS product repository.

The private product repository remains the source of truth for:

- Core application code
- Internal infrastructure
- Proprietary integrations
- Environment-specific implementation details
- Deployment logic and operational secrets

This public repository is intended for material that benefits from being shared openly without exposing sensitive or proprietary internals.

## Public vs Private Boundary

The working rule for this repository is simple:

- Public: documentation, roadmap, examples, sanitized sample outputs, reusable policy ideas, community discussions, and future open-source utilities
- Private: production logic, internal architecture details that should not be exposed, customer-specific integrations, infrastructure code, secrets, credentials, and tenant data

If code is published here in the future, it will be limited to intentionally open-source components.

## Project Status

This repository is in an early public setup stage. The core product exists privately, while the public documentation and open-source surface are being shaped here.

That means the roadmap and repository contents will continue to evolve.

## Get Involved

- Browse the [docs](docs/README.md)
- Explore the [examples](examples/demo-seed/README.md)
- Read the [roadmap](ROADMAP.md)
- Review [contribution guidelines](CONTRIBUTING.md)
- Report security concerns through [SECURITY.md](SECURITY.md)
- Open an issue for bugs, ideas, or product feedback

## License

MIT. See [LICENSE](LICENSE).
