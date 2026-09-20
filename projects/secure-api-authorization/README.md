# Secure API Authorization Demo

A compact Python example of **object-level authorization**.

The main security rule is simple: knowing or guessing a resource ID is not enough to access it. A user must own the resource, or have an authorized administrator role.

## Why this matters

APIs often check whether someone is signed in but forget to verify whether that person is allowed to access a specific object. That can lead to broken object-level authorization / IDOR-style vulnerabilities.

This project keeps authentication and authorization separate and makes the authorization decision explicit and testable.

## Test it

```bash
python -m unittest test_authz.py
```

## What the tests cover

- the resource owner can read
- another authenticated user is denied
- an authorized administrator can update
