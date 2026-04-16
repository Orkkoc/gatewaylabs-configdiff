# How It Works

ConfigDiff is built around a workflow that turns configuration comparison into an operational control loop.

## 1. Define a Known-Good Baseline

Start with a trusted configuration state for an environment pair such as PROD and TEST. That baseline can come from a release-ready repository state or a clean snapshot.

The baseline matters because drift only has meaning when there is a clear reference point.

## 2. Compare Environments Repeatedly

Run comparisons between environments instead of relying on release-day spot checks.

Typical comparison sources include:

- repository-backed configuration
- environment snapshots
- bundled configuration archives

## 3. Surface Meaningful Drift

The comparison highlights what changed:

- missing keys
- extra keys
- changed values

Useful workflows usually include masking, ignore rules, and validation rules so the output stays actionable.

## 4. Turn Drift Into Follow-Through

The operational value comes after the diff:

- store the result
- review what changed
- open findings or raise alerts
- apply policy checks in CI/CD or release workflows

## Manual Diff vs Monitoring

Manual comparison is useful for fast inspection.

Monitoring is useful when teams need repeatable drift detection over time, especially across release cycles or private-network environments.

## Example Flow

1. Choose a baseline for PROD
2. Compare TEST against that baseline before release
3. Detect unexpected differences
4. Decide whether the change is valid, risky, or accidental
5. Alert the right owner or block the release path when needed
