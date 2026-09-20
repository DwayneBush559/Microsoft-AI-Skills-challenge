# AI Ticket Router

A small, explainable support-ticket classifier written in Python.

It routes incoming IT tickets into **security**, **network**, **software**, **hardware**, or **general** categories and returns the terms that influenced the result.

## Why I built it

This project demonstrates a simple version of a problem that appears in AI-assisted service desks: taking unstructured text, extracting useful signals, and routing work consistently.

I intentionally kept the first version transparent instead of hiding the decision behind a large model. That makes it easy to test, inspect, and later replace the rule-based scorer with an embedding or trained classifier.

## Run it

```bash
python router.py "Suspicious login and phishing email hit my account"
```

## Test it

```bash
python -m unittest test_router.py
```

## Possible next step

Replace the keyword scorer with a small trained text classifier, compare accuracy, and preserve an explanation layer for each prediction.
