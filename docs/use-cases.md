# Use Cases

## Release Readiness

Compare TEST or UAT against PROD before a deployment window to catch drift that is not visible in source code alone.

## Post-Release Verification

Run a comparison after deployment to confirm the runtime environment still matches the intended state.

## Ongoing Drift Monitoring

Schedule repeated checks so slow operational drift becomes visible before it turns into an outage or rollback.

## Microsoft-Stack Validation

Use ConfigDiff in environments where `.NET`, IIS, `appsettings.json`, and `web.config` are common sources of environment-specific issues.

## Private-Network and Hybrid Operations

Apply the same control model to environments that are not fully cloud-native, not fully declarative, or not fully automated yet.

## Policy-Based Release Gates

Express risky differences as policy rules so CI/CD workflows can warn or fail when protected configuration changes unexpectedly.
