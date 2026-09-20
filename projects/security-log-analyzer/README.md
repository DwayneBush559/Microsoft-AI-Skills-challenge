# Security Log Analyzer

A small Python command-line project that scans text logs for a few common security signals:

- repeated failed logins
- possible brute-force activity
- SQL-injection strings
- path traversal
- basic script-injection patterns

The output is structured JSON so it can be sent to another script, dashboard, or incident-response workflow.

## Run it

```bash
python analyzer.py sample.log
```

## Test it

```bash
python -m unittest test_analyzer.py
```

## What this demonstrates

The goal is not to replace a SIEM. It demonstrates log parsing, rule-based detection, severity scoring, structured output, and basic test coverage in a compact project that is easy to review.
