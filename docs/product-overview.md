# Product Overview

## Summary

ConfigDiff helps teams detect configuration drift between environments before it becomes a release blocker, production incident, or compliance gap.

The product is designed around a simple idea: compare environments against a known-good baseline, then make drift visible in a way teams can actually act on.

## Problem

Many teams do not operate in a fully GitOps or fully immutable world. Configuration still changes through manual fixes, partial automation, environment-specific overrides, and legacy operational processes.

That creates a common failure mode:

- code looks correct
- deployment looks successful
- production still behaves differently because configuration drifted

Manual checks are slow, inconsistent, and easy to skip when release pressure is high.

## Product Approach

ConfigDiff is positioned as a baseline-aware configuration drift monitoring product.

It is not just a one-off diff utility. Manual comparison is one entry point, but the broader value is ongoing drift detection and operational follow-through.

## Key Capabilities

- Compare environments such as PROD, UAT, and TEST
- Use a known-good baseline as the reference point
- Detect added, removed, and changed configuration values
- Keep drift visible through reports, findings, and history
- Support alerts and policy-driven workflows
- Fit CI/CD and release validation processes

## Best Fit

ConfigDiff is best suited for:

- DevOps, platform, and release teams
- .NET and IIS-heavy environments
- Azure DevOps-oriented teams
- hybrid, legacy, or partially automated estates

## What It Is Not

ConfigDiff is not:

- a GitOps replacement
- a configuration management platform
- an automatic remediation system
- a generic text diff tool with no operational workflow

## Why the Public Repo Exists

The core product lives in a private repository. This public repository exists to share:

- product explanation
- technical concepts
- roadmap direction
- sanitized examples
- future open-source companion artifacts
