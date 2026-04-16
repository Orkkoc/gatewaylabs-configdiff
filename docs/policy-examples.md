# Policy Examples

Policy rules help teams define which configuration differences are acceptable and which ones should trigger review or failure.

## Example Rule Style

The examples below illustrate the kind of policy checks ConfigDiff is designed to support:

```txt
rule "No missing keys" when count(missing) > 0 then fail
rule "Block secret changes" when changed("*Password*") or changed("*Token*") then fail
rule "Warn on extras" when count(extra) > 0 then warn
rule "Only allow FeatureFlags" when not changed("FeatureFlags:*") then fail
```

## Practical Patterns

### Protect Sensitive Settings

Fail when secrets, tokens, or connection-related values change unexpectedly.

### Allow Low-Risk Feature Flag Movement

Warn or allow differences in explicitly scoped feature flag keys while blocking everything else.

### Stop Releases on Missing Required Keys

Treat missing production-critical settings as a hard failure condition.

### Flag Runtime-Only Drift

Open a warning when extra keys appear in live environments but do not exist in the expected baseline.

## Why Policies Matter

Diffs tell you what changed.

Policies help teams decide what the change means.
