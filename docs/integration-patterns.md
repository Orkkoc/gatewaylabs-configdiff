# Integration Patterns

This repository does not publish the private product implementation, but the product direction is built around a few common workflow patterns.

## CI/CD Gate

Use configuration comparison as part of a pipeline before promotion or release approval.

Typical outcome:

- generate a comparison result
- evaluate policy rules
- warn or fail when protected configuration changed

## Scheduled Monitoring

Run comparisons on a schedule so drift is detected outside deployment windows as well.

Typical outcome:

- compare against a known-good baseline
- store the result
- raise a finding or alert when drift appears

## Pull Request or Change Review Support

Attach a comparison result to a review workflow so teams can see whether an environment-critical change needs explicit approval.

## Example GitHub Actions Shape

```yaml
name: configdiff

on:
  pull_request:
    paths:
      - "configs/**"

jobs:
  diff:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - name: Run comparison
        run: |
          configdiff diff \
            --left ./configs/prod \
            --right ./configs/test \
            --report ./configdiff-report.html
```

This example is illustrative. Public packaging details for any CLI or companion tooling will be documented separately if they are published.
