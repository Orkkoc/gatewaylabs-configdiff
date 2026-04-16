# Sample Drift Report

This file shows the expected differences for the demo seed example.

## Compared Inputs

- Baseline: `examples/demo-seed/live/prod-clean`
- Drifted target: `examples/demo-seed/live/prod-drift`

## Summary

- Missing keys: `0`
- Extra keys: `1`
- Changed values: `2`

## Changed Values

### appsettings.json

- `ApiBaseUrl`
  - baseline: `https://api.gatewaylabs.local`
  - drifted: `https://api-drained.gatewaylabs.local`

- `FeatureFlags.DebugMode`
  - baseline: `false`
  - drifted: `true`

## Extra Keys

### web.config

- `GatewayLabs.LiveMarker`
  - drifted value: `drifted`

## Why This Example Matters

The drift is intentionally small, but it shows three common categories of operational risk:

- endpoint differences
- unsafe feature-flag changes
- runtime-only config appearing outside the baseline
