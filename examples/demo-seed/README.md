# Demo Seed Example

This example gives the public repository a small, sanitized drift story that is easy to understand without exposing any customer or production data.

## Structure

- `repo/prod` and `repo/test` represent the expected repository-backed environments
- `live/prod-clean` matches the intended production baseline
- `live/prod-drift` introduces a small but meaningful runtime drift

## Suggested Walkthrough

1. Review the repository-backed files under `repo/`
2. Treat `live/prod-clean` as the expected production state
3. Compare `live/prod-drift` against that clean state
4. Inspect the resulting differences in [../sample-drift-report.md](../sample-drift-report.md)

## Intended Drift

The drifted example intentionally changes:

- `ApiBaseUrl`
- `FeatureFlags.DebugMode`
- `GatewayLabs.LiveMarker` in `web.config`

That creates a compact example with:

- one value change
- one risky feature-flag flip
- one extra runtime-only marker
